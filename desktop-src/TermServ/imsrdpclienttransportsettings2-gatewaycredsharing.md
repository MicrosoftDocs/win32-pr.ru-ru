---
title: IMsRdpClientTransportSettings2 Гатевайкредшаринг, свойство
description: Указывает или получает параметр, указывающий, включена ли функция общего доступа к учетным данным шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: 296dc578-376d-41f6-988a-286fe744959f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Гатевайкредшаринг
- Службы удаленных рабочих столов свойства Гатевайкредшаринг, интерфейс IMsRdpClientTransportSettings2
- Службы удаленных рабочих столов интерфейса IMsRdpClientTransportSettings2, свойство Гатевайкредшаринг
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayCredSharing
- IMsRdpClientTransportSettings2.get_GatewayCredSharing
- IMsRdpClientTransportSettings2.put_GatewayCredSharing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 329e425631b674e050f246c4105115bd4326be3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489519"
---
# <a name="imsrdpclienttransportsettings2gatewaycredsharing-property"></a>Свойство IMsRdpClientTransportSettings2:: Гатевайкредшаринг

Указывает или получает параметр, указывающий, включена ли функция общего доступа к учетным данным шлюза удаленный рабочий стол (шлюз удаленных рабочих столов). Если эта функция включена, удаленный рабочий стол элемент управления ActiveX пытается использовать те же учетные данные для проверки подлинности на сервере узла сеансов удаленный рабочий стол (узел сеансов удаленных рабочих столов) и на сервере шлюза удаленных рабочих столов.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_GatewayCredSharing(
  [in]  ULONG ulProxyCredSharing
);

HRESULT get_GatewayCredSharing(
  [out] ULONG *pulProxyCredSharing
);
```



## <a name="property-value"></a>Значение свойства

Если задано значение One, совместное использование учетных данных включено. Если задано значение 0, совместное использование учетных данных отключено.

## <a name="error-codes"></a>Коды ошибок

При успешном выполнении возвращает значение **\_ ОК** .

## <a name="remarks"></a>Комментарии

Это свойство используется элементом управления ActiveX для реализации единого запроса на обмен учетными данными между сервером узла сеансов удаленных рабочих столов и сервером шлюза удаленных рабочих столов. Совместное использование учетных данных не поддерживает общий доступ к паролю с использованием [**гатевайпассворд**](imsrdpclienttransportsettings2-gatewaypassword.md) или [**клеартекстпассворд**](imstscnonscriptable-cleartextpassword.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista с пакетом обновления 1 (SP1)<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                    |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>            |
| IID<br/>                      | IID \_ IMsRdpClientTransportSettings2 определен как 67341688-D606-4c73-A5D2-2E0489009319<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиенттранспортсеттингс**](imsrdpclienttransportsettings.md)
</dt> <dt>

[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





