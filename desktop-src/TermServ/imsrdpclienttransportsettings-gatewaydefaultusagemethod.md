---
title: Имсрдпклиенттранспортсеттингс Гатевайдефаултусажемесод, свойство
description: Метод использования по умолчанию для шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайдефаултусажемесод
- Службы удаленных рабочих столов свойства Гатевайдефаултусажемесод, интерфейс Имсрдпклиенттранспортсеттингс
- Службы удаленных рабочих столов интерфейса Имсрдпклиенттранспортсеттингс, свойство Гатевайдефаултусажемесод
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6403f319eaa79b9d140a3d75f9dd4f7625eced916ee907755c017d3e58a1767f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118607425"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a>Свойство Имсрдпклиенттранспортсеттингс:: Гатевайдефаултусажемесод

Метод использования по умолчанию для шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a>Значение свойства

Указатель на метод использования по умолчанию для шлюза удаленных рабочих столов. Возвращает объединение пользовательских параметров, заданных параметрами SET [**\_ гатевайусажемесод ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)и групповой политики. Если параметры пользователя не были заданы методом set **\_ гатевайусажемесод ()**, **Get \_ гатевайдефаултусажемесод ()** вернет значение по умолчанию, равное **таймеру TSC для \_ \_ \_ обнаружения в режиме прокси**.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                         |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                   |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ имсрдпклиенттранспортсеттингс определен как 720298C0-A099-46f5-9F82-96921BAE4701<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





