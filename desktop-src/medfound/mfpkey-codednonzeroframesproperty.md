---
description: Указывает количество видеокадров, закодированных кодеком, который фактически содержит данные.
ms.assetid: f96fd0b2-8c81-4318-b44c-4b794b3945a3
title: Свойство MFPKEY_CODEDNONZEROFRAMES (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b1ca5fb26288e2ea9ff801ba13aa7bef570ca95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711943"
---
# <a name="mfpkey_codednonzeroframes-property"></a>МФПКЭЙ \_ кодеднонзерофрамес, свойство

Указывает количество видеокадров, закодированных кодеком, который фактически содержит данные.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

VT \_ I4

## <a name="remarks"></a>Комментарии

Это значение равно [мфпкэй \_ тоталфрамес](mfpkey-totalframesproperty.md) минус все кадры, которые были удалены из-за ограничений битовой частоты, за вычетом кадров нулевых байтов. Это значение можно получить после завершения передачи образцов. Для повторяющихся кадров можно создавать кадры нулевого байта.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
