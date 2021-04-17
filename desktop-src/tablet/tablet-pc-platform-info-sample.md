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
# <a name="tablet-pc-platform-info-sample"></a><span data-ttu-id="cf419-103">Пример сведений о платформе Tablet PC</span><span class="sxs-lookup"><span data-stu-id="cf419-103">Tablet PC Platform Info Sample</span></span>

<span data-ttu-id="cf419-104">Эта программа проверяет наличие и настройку основных компонентов Микрософттаблет ПК и технологии сенсорного программирования.</span><span class="sxs-lookup"><span data-stu-id="cf419-104">This program checks the presence and configuration of the MicrosoftTablet PC and Touch Technology core components.</span></span> <span data-ttu-id="cf419-105">Он определяет, включены ли компоненты планшетных ПК в операционной системе, выводит список имен и сведений о версиях для основных элементов управления, а также распознавания рукописного текста и речи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf419-105">It determines whether Tablet PC components are enabled in the operating system, listing names and version information for core controls and the default handwriting and speech recognizer.</span></span>

<span data-ttu-id="cf419-106">Приложение использует API Windows Жетсистемметрикс, передавая значение SM \_ TABLETPC, чтобы определить, работает ли приложение на планшетном ПК.</span><span class="sxs-lookup"><span data-stu-id="cf419-106">The application uses the GetSystemMetrics Windows API, passing in SM\_TABLETPC, to determine whether the application running on a Tablet PC.</span></span> <span data-ttu-id="cf419-107">SM \_ TABLETPC определен в файле WinUser. h.</span><span class="sxs-lookup"><span data-stu-id="cf419-107">SM\_TABLETPC is defined in WinUser.h.</span></span>

<span data-ttu-id="cf419-108">Определенный интерес заключается в том, как приложение использует коллекцию распознавателей для предоставления сведений о распознавателе по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cf419-108">Of particular interest is the way the application uses the Recognizers collection to provide information about the default recognizer.</span></span> <span data-ttu-id="cf419-109">Прежде чем пытаться использовать коллекцию распознавателей и объект распознавателя, приложение проверяет успешное создание.</span><span class="sxs-lookup"><span data-stu-id="cf419-109">Before attempting to use the Recognizers collection and Recognizer object, the application tests for their successful creation.</span></span>

## <a name="components"></a><span data-ttu-id="cf419-110">Компоненты</span><span class="sxs-lookup"><span data-stu-id="cf419-110">Components</span></span>

<span data-ttu-id="cf419-111">Используя повторно распространяемый модуль слияния, некоторые части API платформы Tablet PC могут быть установлены в версиях Vista и Windows XP Professional, отличных от планшета.</span><span class="sxs-lookup"><span data-stu-id="cf419-111">Using the re-distributable merge module, certain parts of the Tablet PC Platform API may be installed on non-Tablet versions of Vista and Windows XP Professional .</span></span> <span data-ttu-id="cf419-112">Вызов Жетсистемметрикс означает, что установлен Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="cf419-112">The GetSystemMetrics call only indicates that Windows XP Tablet PC Edition is installed.</span></span> <span data-ttu-id="cf419-113">Приложение должно всегда определять, доступен ли данный компонент.</span><span class="sxs-lookup"><span data-stu-id="cf419-113">An application should always determine if a given component is available.</span></span> <span data-ttu-id="cf419-114">Правильный способ определить, установлен ли компонент API, — попытаться создать экземпляр объекта или элемента управления и проверить, что он существует, прежде чем пытаться использовать его, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="cf419-114">The proper way to determine if a component of the API is installed is to attempt to create an instance of an object or control and check that it exists before attempting to use it, as shown in the following example.</span></span>


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



<span data-ttu-id="cf419-115">Приложение обнаруживает сведения об установленных компонентах речи, просматривая соответствующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="cf419-115">The application finds out about the installed speech components by looking in the appropriate registry key:</span></span>


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



<span data-ttu-id="cf419-116">Ключ считывается с помощью Регкуеривалуиксв.</span><span class="sxs-lookup"><span data-stu-id="cf419-116">The key is read using RegQueryValueExW.</span></span>

<span data-ttu-id="cf419-117">Наконец, образец определяет, какие элементы управления установлены.</span><span class="sxs-lookup"><span data-stu-id="cf419-117">Finally, the sample finds out which controls are installed.</span></span>


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



 

 



