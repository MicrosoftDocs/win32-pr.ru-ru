---
title: Имсрдпклиентадванцедсеттингс Коннекттосерверконсоле, свойство
description: Данное свойство не поддерживается. Вызовы Коннекттосерверконсоле всегда возвращают \_ значение false.
ms.assetid: 58f79085-4364-408f-8bf1-97a82ad68f4b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннекттосерверконсоле
- Службы удаленных рабочих столов свойства Коннекттосерверконсоле, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Коннекттосерверконсоле
- Службы удаленных рабочих столов свойства Коннекттосерверконсоле, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Коннекттосерверконсоле
- Службы удаленных рабочих столов свойства Коннекттосерверконсоле, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Коннекттосерверконсоле
- Службы удаленных рабочих столов свойства Коннекттосерверконсоле, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Коннекттосерверконсоле
- Службы удаленных рабочих столов свойства Коннекттосерверконсоле, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Коннекттосерверконсоле
- Службы удаленных рабочих столов свойства Коннекттосерверконсоле, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Коннекттосерверконсоле
- Службы удаленных рабочих столов свойства Коннекттосерверконсоле, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Коннекттосерверконсоле
- Службы удаленных рабочих столов свойства Коннекттосерверконсоле, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Коннекттосерверконсоле
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ConnectToServerConsole
- IMsRdpClientAdvancedSettings.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.put_ConnectToServerConsole
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83c6b935c34dda3f8a676d025bc1995a30e1bbb3f11dd4db3c055f6e28437ba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515284"
---
# <a name="imsrdpclientadvancedsettingsconnecttoserverconsole-property"></a>Свойство Имсрдпклиентадванцедсеттингс:: Коннекттосерверконсоле

Данное свойство не поддерживается. Вызовы **коннекттосерверконсоле** всегда возвращают **\_ значение false**.

Используйте свойство [**коннекттоадминистерсервер**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) для подключения к сеансу, который используется для административных целей.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ConnectToServerConsole(
  [in]  VARIANT_BOOL connectToServerConsole
);

HRESULT get_ConnectToServerConsole(
  [out] VARIANT_BOOL *pconnectToServerConsole
);
```



## <a name="property-value"></a>Значение свойства

Присвойте этому параметру значение **Variant \_ false**. **Вариант \_ Значение TRUE** не поддерживается.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ имсрдпклиентадванцедсеттингс определен как 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>См. также

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

 

 





