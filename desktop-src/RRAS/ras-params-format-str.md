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
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136374"
---
# <a name="ras_params_format-enumeration"></a>\_ \_ Перечисление форматов параметров RAS

\[Перечисление **\_ \_ форматов параметров RAS** не поддерживается в Windows Vista.\]

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                           |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                 |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Рассапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Обзор службы удаленного доступа (RAS)](about-remote-access-service.md)
</dt> <dt>

[Перечисления для администрирования сервера RAS](ras-server-administration-enumerations.md)
</dt> <dt>

[**\_Параметры RAS**](ras-parameters-str.md)
</dt> </dl>

 

 





