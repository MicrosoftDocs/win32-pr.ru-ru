---
description: Эта программа проверяет наличие и настройку основных компонентов Микрософттаблет ПК и технологии сенсорного программирования.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Пример сведений о платформе Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d815f21233b1edcc90d456df68b3736c170a5fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693565"
---
# <a name="tablet-pc-platform-info-sample"></a>Пример сведений о платформе Tablet PC

Эта программа проверяет наличие и настройку основных компонентов Микрософттаблет ПК и технологии сенсорного программирования. Он определяет, включены ли компоненты планшетных ПК в операционной системе, выводит список имен и сведений о версиях для основных элементов управления, а также распознавания рукописного текста и речи по умолчанию.

Приложение использует API Windows Жетсистемметрикс, передавая значение SM \_ TABLETPC, чтобы определить, работает ли приложение на планшетном ПК. SM \_ TABLETPC определен в файле WinUser. h.

Определенный интерес заключается в том, как приложение использует коллекцию распознавателей для предоставления сведений о распознавателе по умолчанию. Прежде чем пытаться использовать коллекцию распознавателей и объект распознавателя, приложение проверяет успешное создание.

## <a name="components"></a>Компоненты

Используя повторно распространяемый модуль слияния, некоторые части API платформы Tablet PC могут быть установлены в версиях Vista и Windows XP Professional, отличных от планшета. Вызов Жетсистемметрикс означает, что установлен Windows XP Tablet PC Edition. Приложение должно всегда определять, доступен ли данный компонент. Правильный способ определить, установлен ли компонент API, — попытаться создать экземпляр объекта или элемента управления и проверить, что он существует, прежде чем пытаться использовать его, как показано в следующем примере.


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



 

 



