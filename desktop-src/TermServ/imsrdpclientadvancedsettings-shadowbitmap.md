---
title: Имсрдпклиентадванцедсеттингс Шадовбитмап, свойство
description: Указывает, следует ли использовать теневые растровые изображения.
ms.assetid: b329e367-7579-466d-877a-16253f85e5a2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Шадовбитмап
- Службы удаленных рабочих столов свойства Шадовбитмап, интерфейс Имсрдпклиентадванцедсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиентадванцедсеттингс, свойство Шадовбитмап
- Службы удаленных рабочих столов свойства Шадовбитмап, интерфейс IMsRdpClientAdvancedSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings2, свойство Шадовбитмап
- Службы удаленных рабочих столов свойства Шадовбитмап, интерфейс IMsRdpClientAdvancedSettings3
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings3, свойство Шадовбитмап
- Службы удаленных рабочих столов свойства Шадовбитмап, интерфейс IMsRdpClientAdvancedSettings4
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings4, свойство Шадовбитмап
- Службы удаленных рабочих столов свойства Шадовбитмап, интерфейс IMsRdpClientAdvancedSettings5
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings5, свойство Шадовбитмап
- Службы удаленных рабочих столов свойства Шадовбитмап, интерфейс IMsRdpClientAdvancedSettings6
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings6, свойство Шадовбитмап
- Службы удаленных рабочих столов свойства Шадовбитмап, интерфейс IMsRdpClientAdvancedSettings7
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings7, свойство Шадовбитмап
- Службы удаленных рабочих столов свойства Шадовбитмап, интерфейс IMsRdpClientAdvancedSettings8
- Службы удаленных рабочих столов интерфейса IMsRdpClientAdvancedSettings8, свойство Шадовбитмап
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ShadowBitmap
- IMsRdpClientAdvancedSettings.get_ShadowBitmap
- IMsRdpClientAdvancedSettings.put_ShadowBitmap
- IMsRdpClientAdvancedSettings2.ShadowBitmap
- IMsRdpClientAdvancedSettings2.get_ShadowBitmap
- IMsRdpClientAdvancedSettings2.put_ShadowBitmap
- IMsRdpClientAdvancedSettings3.ShadowBitmap
- IMsRdpClientAdvancedSettings3.get_ShadowBitmap
- IMsRdpClientAdvancedSettings3.put_ShadowBitmap
- IMsRdpClientAdvancedSettings4.ShadowBitmap
- IMsRdpClientAdvancedSettings4.get_ShadowBitmap
- IMsRdpClientAdvancedSettings4.put_ShadowBitmap
- IMsRdpClientAdvancedSettings5.ShadowBitmap
- IMsRdpClientAdvancedSettings5.get_ShadowBitmap
- IMsRdpClientAdvancedSettings5.put_ShadowBitmap
- IMsRdpClientAdvancedSettings6.ShadowBitmap
- IMsRdpClientAdvancedSettings6.get_ShadowBitmap
- IMsRdpClientAdvancedSettings6.put_ShadowBitmap
- IMsRdpClientAdvancedSettings7.ShadowBitmap
- IMsRdpClientAdvancedSettings7.get_ShadowBitmap
- IMsRdpClientAdvancedSettings7.put_ShadowBitmap
- IMsRdpClientAdvancedSettings8.ShadowBitmap
- IMsRdpClientAdvancedSettings8.get_ShadowBitmap
- IMsRdpClientAdvancedSettings8.put_ShadowBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04e41845bc3c7ebb32b5b6300c5ccd1bc9d1444ef86497e613bc833c220cec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757441"
---
# <a name="imsrdpclientadvancedsettingsshadowbitmap-property"></a>Свойство Имсрдпклиентадванцедсеттингс:: Шадовбитмап

\[Данное свойство не поддерживается. начиная с Windows Server 2008 и Windows 7 вызовы **шадовбитмап** всегда возвращают **\_ значение FALSE**.\]

Указывает, следует ли использовать теневые растровые изображения.

Теневые растровые изображения всегда отключены в полноэкранном режиме, поэтому это свойство не действует в полноэкранном режиме.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ShadowBitmap(
  [in]  LONG shadowBitmap
);

HRESULT get_ShadowBitmap(
  [out] LONG *pshadowBitmap
);
```



## <a name="property-value"></a>Значение свойства

Задайте для этого параметра значение 0, чтобы отключить функцию, или ненулевое, чтобы включить эту функцию. Отключение этой функции обычно повышает производительность, но может привести к появлению артефактов при рисовании экранов.

## <a name="remarks"></a>Remarks

Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                        |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                       |
| Окончание поддержки клиента<br/>    | Windows Vista<br/>                                                                        |
| Поддержка конца сервера<br/>    | Ни одна версия не поддерживается<br/>                                                                       |
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

 

 





