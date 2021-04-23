---
description: Интерфейс Ихвевенсандлер может быть зарегистрирован в запущенной таблице объектов, чтобы у запущенных приложений был доступ к событиям автозапуска.
ms.assetid: 6FEFFB5D-DD8B-4FEA-B273-D32FC30CAFEA
title: Использование событий автозапуска в выполняющихся приложениях
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51795a3992bdb40dde833bb3e352905efaa2be63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998446"
---
# <a name="how-to-use-autoplay-events-in-running-applications"></a><span data-ttu-id="a3d4e-103">Использование событий автозапуска в выполняющихся приложениях</span><span class="sxs-lookup"><span data-stu-id="a3d4e-103">How to Use AutoPlay Events in Running Applications</span></span>

<span data-ttu-id="a3d4e-104">Интерфейс [**ихвевенсандлер**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) может быть зарегистрирован в запущенной таблице объектов, чтобы у запущенных приложений был доступ к событиям автозапуска.</span><span class="sxs-lookup"><span data-stu-id="a3d4e-104">The [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface can be registered in the running object table (ROT) so that running applications have access to AutoPlay events.</span></span>

<span data-ttu-id="a3d4e-105">Следующие инструкции описывают, как использовать события автозапуска в выполняющихся приложениях.</span><span class="sxs-lookup"><span data-stu-id="a3d4e-105">The following instructions describe how to use AutoPlay events in running applications.</span></span>

## <a name="instructions"></a><span data-ttu-id="a3d4e-106">Инструкции</span><span class="sxs-lookup"><span data-stu-id="a3d4e-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="a3d4e-107">Шаг 1.</span><span class="sxs-lookup"><span data-stu-id="a3d4e-107">Step 1:</span></span>

<span data-ttu-id="a3d4e-108">Создайте новый компонент, реализующий интерфейс [**ихвевенсандлер**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="a3d4e-108">Create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="a3d4e-109">Шаг 2.</span><span class="sxs-lookup"><span data-stu-id="a3d4e-109">Step 2:</span></span>

<span data-ttu-id="a3d4e-110">Инициализируйте новый компонент со значением Иниткмдлине из записи конкретного обработчика в разделе **обработчиков** .</span><span class="sxs-lookup"><span data-stu-id="a3d4e-110">Initialize the new component with the InitCmdLine value from the particular handler's entry under the **Handlers** key.</span></span>

<span data-ttu-id="a3d4e-111">Этот шаг является обязательным, поскольку автозапуск не вызывает метод Initialize.</span><span class="sxs-lookup"><span data-stu-id="a3d4e-111">This step is required because Autoplay does not call the Initialize method.</span></span>

### <a name="step-3"></a><span data-ttu-id="a3d4e-112">Шаг 3.</span><span class="sxs-lookup"><span data-stu-id="a3d4e-112">Step 3:</span></span>

<span data-ttu-id="a3d4e-113">Вызовите функцию [**креатехардваривентмоникер**](createhardwareeventmoniker.md) , чтобы получить моникер, представляющий ваш компонент и обработчик событий, который необходимо вызвать.</span><span class="sxs-lookup"><span data-stu-id="a3d4e-113">Call the [**CreateHardwareEventMoniker**](createhardwareeventmoniker.md) function to get a moniker that represents your component and the event handler that you want to call.</span></span>

### <a name="step-4"></a><span data-ttu-id="a3d4e-114">Шаг 4.</span><span class="sxs-lookup"><span data-stu-id="a3d4e-114">Step 4:</span></span>

<span data-ttu-id="a3d4e-115">Используйте параметр *ппмоникер* для регистрации компонента в таблице ROT.</span><span class="sxs-lookup"><span data-stu-id="a3d4e-115">Use the *ppmoniker* parameter to register your component in the ROT.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3d4e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="a3d4e-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a3d4e-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) может представлять угрозы безопасности.</span><span class="sxs-lookup"><span data-stu-id="a3d4e-117">[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) can pose security risks.</span></span> <span data-ttu-id="a3d4e-118">Сведения о правильной загрузке библиотек DLL с разными версиями Windows см. в документации по **LoadLibrary** .</span><span class="sxs-lookup"><span data-stu-id="a3d4e-118">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

```cpp
typedef HRESULT (*CREATEHARDWAREEVENTMONIKER)(REFCLSID clsid, LPCWSTR pszEventHandler, IMoniker **ppmoniker);

HRESULT RegisterComponent(IUnknown* punk, DWORD* dpwToken)
{
    HRESULT hr = E_FAIL;
    HINSTANCE hinstShSvcs = LoadLibrary(TEXT("shsvcs.dll"));
    
    if (hinstShSvcs)
    {   
        CREATEHARDWAREEVENTMONIKER fct = (CREATEHARDWAREEVENTMONIKER)GetProcAddress(hinstShSvcs, "CreateHardwareEventMoniker");
        if (fct)
        {
            IMoniker* pmoniker;
            
            hr = fct(CLSID_App, TEXT("VideoCameraArrival"), &pmoniker);

            if (SUCCEEDED(hr))
            {
                IRunningObjectTable *prot;
                    
                if (SUCCEEDED(GetRunningObjectTable(0, &prot)))
                {
                    hr = prot->Register(ROTFLAGS_ALLOWANYCLIENT | ROTFLAGS_REGISTRATIONKEEPSALIVE, punk, pmoniker, &_dwRegisterROT);
                    prot->Release();
                }
                pmoniker->Release();
            }
            CoRegisterClassObject(CLSID_App, static_cast<IClassFactory *>(this), CLSCTX_LOCAL_SERVER, REGCLS_MULTIPLEUSE, &_dwRegisterClass;
        }
        FreeLibrary(hinstShSvcs);
    }
    return hr;
}
```

<span data-ttu-id="a3d4e-119">Для вызова [**ируннингобжекттабле:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) необходимо, чтобы компонент имел в реестре следующие сведения о **AppID** .</span><span class="sxs-lookup"><span data-stu-id="a3d4e-119">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that the component have the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="related-topics"></a><span data-ttu-id="a3d4e-120">См. также</span><span class="sxs-lookup"><span data-stu-id="a3d4e-120">Related topics</span></span>

[<span data-ttu-id="a3d4e-121">**ихвевенсандлер**</span><span class="sxs-lookup"><span data-stu-id="a3d4e-121">**IHWEventHandler**</span></span>](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[<span data-ttu-id="a3d4e-122">**креатехардваривентмоникер**</span><span class="sxs-lookup"><span data-stu-id="a3d4e-122">**CreateHardwareEventMoniker**</span></span>](createhardwareeventmoniker.md)
