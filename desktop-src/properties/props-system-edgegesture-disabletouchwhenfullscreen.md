---
description: Предотвращает поведение пограничных жестов при активном окне приложения и в полноэкранном режиме (или в активном окне).
ms.assetid: F4242C05-181B-44FC-BE6C-8ABB76079981
title: System. Еджежестуре. Дисаблетаучвхенфуллскрин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 208962f11b96420a8e0ef771ada846a3f802e815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656690"
---
# <a name="systemedgegesturedisabletouchwhenfullscreen"></a>System. Еджежестуре. Дисаблетаучвхенфуллскрин

Предотвращает поведение пограничных жестов при активном окне приложения и в полноэкранном режиме (или в активном окне).

> [!Note]  
> В полноэкранном режиме размер окна приложения соответствует разрешению экрана.

 

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.EdgeGesture.DisableTouchWhenFullscreen
   shellPKey = PKEY_EdgeGesture_DisableTouchWhenFullscreen
   formatID = 32CE38B2-2C9A-41B1-9BC5-B3784394AA44
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Комментарии

В Windows 8 взаимодействие пользователя с краями экрана показывает пользовательский интерфейс системы, такой как панели приложений, чудо и выполняющиеся приложения.

Для полноэкранных удаленных приложений это поведение пользовательского интерфейса на локальном компьютере может переопределяться и влиять на пользовательский интерфейс удаленного сеанса. Это свойство позволяет приложению отключить ребро пользовательского интерфейса на локальном компьютере.

Чтобы отключить интерфейс ребра, присвойте этому свойству значение \_ true. Значение по умолчанию — VARIANT \_ false.

Это свойство не влияет на приложения Магазина Windows.

В следующем примере показано, как задать пограничные поведения пользовательского интерфейса.


```
HRESULT SetTouchDisableProperty(HWND hwnd, BOOL fDisableTouch)
{
    IPropertyStore* pPropStore;
    HRESULT hrReturnValue = SHGetPropertyStoreForWindow(hwnd, IID_PPV_ARGS(&pPropStore));
    if (SUCCEEDED(hrReturnValue))
    {
        PROPVARIANT var;
        var.vt = VT_BOOL;
        var.boolVal = fDisableTouch ? VARIANT_TRUE : VARIANT_FALSE;
        hrReturnValue = pPropStore->SetValue(PKEY_EdgeGesture_DisableTouchWhenFullscreen, var);
        pPropStore->Release();
    }
    return hrReturnValue;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[пропертидескриптион](./propdesc-schema-propertydescription.md)
</dt> <dt>

[сеарчинфо](./propdesc-schema-searchinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> </dl>

 

 
