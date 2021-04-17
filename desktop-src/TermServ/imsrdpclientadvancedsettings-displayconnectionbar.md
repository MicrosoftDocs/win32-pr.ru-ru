---
title: Имсрдпклиентадванцедсеттингс Дисплайконнектионбар, свойство
description: Указывает, следует ли использовать панель подключения. Значение по умолчанию — VARIANT \_ true, которое включает свойство.
ms.assetid: 251c0322-5589-423d-9694-004f847c173b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дисплайконнектионбар
- Службы удаленных рабочих столов свойства Дисплайконнектионбар, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Дисплайконнектионбар
- Службы удаленных рабочих столов свойства Дисплайконнектионбар, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Дисплайконнектионбар
- Службы удаленных рабочих столов свойства Дисплайконнектионбар, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Дисплайконнектионбар
- Службы удаленных рабочих столов свойства Дисплайконнектионбар, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Дисплайконнектионбар
- Службы удаленных рабочих столов свойства Дисплайконнектионбар, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Дисплайконнектионбар
- Службы удаленных рабочих столов свойства Дисплайконнектионбар, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Дисплайконнектионбар
- Службы удаленных рабочих столов свойства Дисплайконнектионбар, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Дисплайконнектионбар
- Службы удаленных рабочих столов свойства Дисплайконнектионбар, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Дисплайконнектионбар
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisplayConnectionBar
- IMsRdpClientAdvancedSettings.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.put_DisplayConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39dd85d0c8fd578931ed9ca8b85ac7a5ca01981e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681838"
---
# <a name="imsrdpclientadvancedsettingsdisplayconnectionbar-property"></a>Имсрдпклиентадванцедсеттингс: свойство Исплайконнектионбар:D

Указывает, следует ли использовать панель подключения. Значение по умолчанию — **Variant \_ true**, которое включает свойство. Присвоение этому свойству значения **Variant \_ false** в защищенной среде скриптов **возвращает \_ ошибку E**.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_DisplayConnectionBar(
  [in]  VARIANT_BOOL fDisplayConnectionBar
);

HRESULT get_DisplayConnectionBar(
  [out] VARIANT_BOOL *pfDisplayConnectionBar
);
```



## <a name="property-value"></a>Значение свойства

Присвойте этому параметру значение **Variant \_ false** , чтобы отключить функцию или **вариант \_ true** , чтобы включить эту функцию. Значение по умолчанию — **Variant \_ true**.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                        |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                  |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**имсрдпклиентадванцедсеттингс**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





