---
title: Имсрдпдривеколлектион Дривекаунт, свойство
description: Возвращает число объектов в коллекции. | Имсрдпдривеколлектион Дривекаунт, свойство
ms.assetid: 33b39657-2cc1-4f1e-b23a-809a9737ed8d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Дривекаунт
- Службы удаленных рабочих столов свойства Дривекаунт, интерфейс Имсрдпдривеколлектион
- Службы удаленных рабочих столов интерфейса Имсрдпдривеколлектион, свойство Дривекаунт
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveCount
- IMsRdpDriveCollection.get_DriveCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ee79a361e8e24f8b699b8b5fae4aba923d11f62bf512f056a788c15d34d4805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513294"
---
# <a name="imsrdpdrivecollectiondrivecount-property"></a>Имсрдпдривеколлектион: свойство Ривекаунт:D

Возвращает число объектов в коллекции.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_DriveCount(
  [out] ULONG *pDriveCount
);
```



## <a name="property-value"></a>Значение свойства

Число объектов.

## <a name="error-codes"></a>Коды ошибок

Если метод выполнен успешно, возвращается значение **S \_ OK** . Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ имсрдпдривеколлектион определен как 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**имсрдпдривеколлектион**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





