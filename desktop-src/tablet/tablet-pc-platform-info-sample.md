---
description: Эта программа проверяет наличие и настройку основных компонентов Микрософттаблет ПК и технологии сенсорного программирования.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Пример сведений о платформе Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1731fc30e0405b2702bb45d0a9d0556b861ad09994ac683d739da33afe018088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819985"
---
# <a name="tablet-pc-platform-info-sample"></a>Пример сведений о платформе Tablet PC

Эта программа проверяет наличие и настройку основных компонентов Микрософттаблет ПК и технологии сенсорного программирования. Он определяет, включены ли компоненты планшетных ПК в операционной системе, выводит список имен и сведений о версиях для основных элементов управления, а также распознавания рукописного текста и речи по умолчанию.

приложение использует API-интерфейс жетсистемметрикс Windows, передавая значение SM \_ TABLETPC, чтобы определить, работает ли приложение на планшетном пк. SM \_ TABLETPC определен в файле WinUser. h.

Определенный интерес заключается в том, как приложение использует коллекцию распознавателей для предоставления сведений о распознавателе по умолчанию. Прежде чем пытаться использовать коллекцию распознавателей и объект распознавателя, приложение проверяет успешное создание.

## <a name="components"></a>Компоненты

используя повторно распространяемый модуль слияния, некоторые части API платформы Tablet PC могут быть установлены на не планшетных версиях Vista и Windows XP Professional. вызов жетсистемметрикс означает, что установлен только Windows XP Tablet PC Edition. Приложение должно всегда определять, доступен ли данный компонент. Правильный способ определить, установлен ли компонент API, — попытаться создать экземпляр объекта или элемента управления и проверить, что он существует, прежде чем пытаться использовать его, как показано в следующем примере.


```C++
IInkRecognizers* pIInkRecognizers = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkRecognizers,
                              NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IInkRecognizers, 
                              (void **)&pIInkRecognizers);
if (SUCCEEDED(hr)) 
{
  // use the component
} else
{
  // component unavailable
}
```



Приложение обнаруживает сведения об установленных компонентах речи, просматривая соответствующий раздел реестра:


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



Ключ считывается с помощью Регкуеривалуиксв.

Наконец, образец определяет, какие элементы управления установлены.


```C++
LPCOLESTR gc_wszProgId[NUM_CONTROLS] = {L"InkEd.InkEdit", L"msinkaut.InkOverlay"};
// ...
for (int i = 0, j = 0; i < NUM_CONTROLS; i++)
{
    // Get the component info
    CLSID clsid;
    if (SUCCEEDED(CLSIDFromProgID(gc_wszProgId[i], &clsid)) && GetComponentInfo(clsid, info) == TRUE)
    {
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][0], info.wchName);
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][1], info.wchVersion);
        j++;
    }
}
```



 

 



