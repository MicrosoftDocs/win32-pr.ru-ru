---
title: Имсрдпклиентадванцедсеттингс Редиректпортс, свойство
description: Указывает, разрешено ли перенаправление локальных портов (например, COM и LPT).
ms.assetid: 85e1e40d-8da7-4333-ae96-2bfa44479267
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Редиректпортс
- Службы удаленных рабочих столов свойства Редиректпортс, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Редиректпортс
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPorts
- IMsRdpClientAdvancedSettings.get_RedirectPorts
- IMsRdpClientAdvancedSettings.put_RedirectPorts
- IMsRdpClientAdvancedSettings2.RedirectPorts
- IMsRdpClientAdvancedSettings2.get_RedirectPorts
- IMsRdpClientAdvancedSettings2.put_RedirectPorts
- IMsRdpClientAdvancedSettings3.RedirectPorts
- IMsRdpClientAdvancedSettings3.get_RedirectPorts
- IMsRdpClientAdvancedSettings3.put_RedirectPorts
- IMsRdpClientAdvancedSettings4.RedirectPorts
- IMsRdpClientAdvancedSettings4.get_RedirectPorts
- IMsRdpClientAdvancedSettings4.put_RedirectPorts
- IMsRdpClientAdvancedSettings5.RedirectPorts
- IMsRdpClientAdvancedSettings5.get_RedirectPorts
- IMsRdpClientAdvancedSettings5.put_RedirectPorts
- IMsRdpClientAdvancedSettings6.RedirectPorts
- IMsRdpClientAdvancedSettings6.get_RedirectPorts
- IMsRdpClientAdvancedSettings6.put_RedirectPorts
- IMsRdpClientAdvancedSettings7.RedirectPorts
- IMsRdpClientAdvancedSettings7.get_RedirectPorts
- IMsRdpClientAdvancedSettings7.put_RedirectPorts
- IMsRdpClientAdvancedSettings8.RedirectPorts
- IMsRdpClientAdvancedSettings8.get_RedirectPorts
- IMsRdpClientAdvancedSettings8.put_RedirectPorts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95b4747aa5e2663bf98dcac86ba2f928efe1b715ad41ea6f4470610712eaa202
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033274"
---
# <a name="imsrdpclientadvancedsettingsredirectports-property"></a>Свойство Имсрдпклиентадванцедсеттингс:: Редиректпортс

Указывает, разрешено ли перенаправление локальных портов (например, COM и LPT).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RedirectPorts(
  [in]  VARIANT_BOOL redirectPorts
);

HRESULT get_RedirectPorts(
  [out] VARIANT_BOOL *predirectPorts
);
```



## <a name="property-value"></a>Значение свойства

Присвойте этому параметру значение **Variant \_ true** , чтобы разрешить перенаправление или **вариант \_ false** в противном случае. **Вариант \_ Значение TRUE** предложит пользователю подтвердить возможность перенаправления во время подключения в целях безопасности.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Remarks

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                        |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                  |
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

 

 





