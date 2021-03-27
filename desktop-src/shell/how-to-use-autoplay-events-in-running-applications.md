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
# <a name="how-to-use-autoplay-events-in-running-applications"></a>Использование событий автозапуска в выполняющихся приложениях

Интерфейс [**ихвевенсандлер**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) может быть зарегистрирован в запущенной таблице объектов, чтобы у запущенных приложений был доступ к событиям автозапуска.

Следующие инструкции описывают, как использовать события автозапуска в выполняющихся приложениях.

## <a name="instructions"></a>Инструкции

### <a name="step-1"></a>Шаг 1.

Создайте новый компонент, реализующий интерфейс [**ихвевенсандлер**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .

### <a name="step-2"></a>Шаг 2.

Инициализируйте новый компонент со значением Иниткмдлине из записи конкретного обработчика в разделе **обработчиков** .

Этот шаг является обязательным, поскольку автозапуск не вызывает метод Initialize.

### <a name="step-3"></a>Шаг 3.

Вызовите функцию [**креатехардваривентмоникер**](createhardwareeventmoniker.md) , чтобы получить моникер, представляющий ваш компонент и обработчик событий, который необходимо вызвать.

### <a name="step-4"></a>Шаг 4.

Используйте параметр *ппмоникер* для регистрации компонента в таблице ROT.

## <a name="remarks"></a>Примечания

> [!Note]  
> [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) может представлять угрозы безопасности. Сведения о правильной загрузке библиотек DLL с разными версиями Windows см. в документации по **LoadLibrary** .

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

Для вызова [**ируннингобжекттабле:: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) необходимо, чтобы компонент имел в реестре следующие сведения о **AppID** .

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

## <a name="related-topics"></a>См. также

[**ихвевенсандлер**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler)

[**креатехардваривентмоникер**](createhardwareeventmoniker.md)
