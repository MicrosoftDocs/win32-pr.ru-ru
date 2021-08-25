---
title: Перечисление RAS_PARAMS_FORMAT (Рассапи. h)
description: '\_ \_ Тип перечисления "Параметры RAS" используется в \_ структуре параметров RAS для указания типа данных, связанных с ключом, относящимся к носителю.'
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS перечисления RAS_PARAMS_FORMAT
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b798ef8a5257afcb4e4ad653801bda0d21691057abad970d6e8158f592146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673184"
---
# <a name="ras_params_format-enumeration"></a>\_ \_ Перечисление форматов параметров RAS

\[перечисление **\_ \_ форматов параметров RAS** не поддерживается в Windows Vista.\]

Тип перечисления "Параметры **RAS \_ \_** " используется в структуре [**\_ параметров RAS**](ras-parameters-str.md) для указания типа данных, связанных с ключом, относящимся к носителю.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**парамнумбер**
</dt> <dd>

Указывает, что данные, связанные с ключом, являются числом.

</dd> <dt>

<span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**парамстринг**
</dt> <dd>

Указывает, что данные, связанные с ключом, являются строкой.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                       |
| Заголовок<br/>                   | <dl> <dt>Рассапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Обзор службы удаленного доступа (RAS)](about-remote-access-service.md)
</dt> <dt>

[Перечисления для администрирования сервера RAS](ras-server-administration-enumerations.md)
</dt> <dt>

[**\_Параметры RAS**](ras-parameters-str.md)
</dt> </dl>

 

 





