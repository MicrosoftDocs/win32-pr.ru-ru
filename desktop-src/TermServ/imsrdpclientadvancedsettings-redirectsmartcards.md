---
title: Имсрдпклиентадванцедсеттингс Редиректсмарткардс, свойство
description: Указывает, разрешено ли перенаправление смарт-карт.
ms.assetid: 53b6b483-ccba-41eb-a417-241a4430958e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Редиректсмарткардс
- Службы удаленных рабочих столов свойства Редиректсмарткардс, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Редиректсмарткардс
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectSmartCards
- IMsRdpClientAdvancedSettings.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.RedirectSmartCards
- IMsRdpClientAdvancedSettings2.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.RedirectSmartCards
- IMsRdpClientAdvancedSettings3.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.RedirectSmartCards
- IMsRdpClientAdvancedSettings4.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.RedirectSmartCards
- IMsRdpClientAdvancedSettings5.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.RedirectSmartCards
- IMsRdpClientAdvancedSettings6.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.RedirectSmartCards
- IMsRdpClientAdvancedSettings7.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.RedirectSmartCards
- IMsRdpClientAdvancedSettings8.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.put_RedirectSmartCards
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0044ba51e9eb0b3987ec337536e288f1687e04d7838e61a9bbcbae2a2176c003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118608403"
---
# <a name="imsrdpclientadvancedsettingsredirectsmartcards-property"></a>Свойство Имсрдпклиентадванцедсеттингс:: Редиректсмарткардс

Указывает, разрешено ли перенаправление смарт-карт.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RedirectSmartCards(
  [in]  VARIANT_BOOL redirectSmartCards
);

HRESULT get_RedirectSmartCards(
  [out] VARIANT_BOOL *predirectSmartCards
);
```



## <a name="property-value"></a>Значение свойства

Присвойте этому параметру значение **Variant \_ true** , чтобы разрешить перенаправление или **вариант \_ false** в противном случае. **Вариант \_ Значение TRUE** предложит пользователю подтвердить возможность перенаправления во время подключения в целях безопасности.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Remarks

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

 

 





