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
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681804"
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

 

 





