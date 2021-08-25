---
title: Структура RAS_PARAMETERS (Рассапи. h)
description: '\_Структура параметров RAS используется функцией расадминпортжетинфо для возврата имени и значения параметра носителя, связанного с портом на сервере удаленного доступа.'
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS структуры RAS_PARAMETERS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e38ec1a8febbca4319a9c098eafee3705fe59602af81b3ec94e4e974892be771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909674"
---
# <a name="ras_parameters-structure"></a>\_Структура параметров RAS

\[структура **\_ параметров RAS** не поддерживается Windows Vista.\]

Структура **\_ параметров RAS** используется функцией [**расадминпортжетинфо**](rasadminportgetinfo.md) для возврата имени и значения параметра носителя, связанного с портом на сервере удаленного доступа.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a>Члены

<dl> <dt>

**\_Ключ P**
</dt> <dd>

Указывает имя ключа, представляющего параметр, относящийся к носителю, например МАКСКОННЕКТБПС.

</dd> <dt>

**\_Тип P**
</dt> <dd>

Определяет тип данных, связанных с параметром. Этот элемент может принимать одно из следующих значений из перечисления [**\_ \_ формата параметров RAS**](ras-params-format-str.md) .



| Значение                                                                                                                                                                                | Значение                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | Указывает, что данные, связанные с ключом, являются числом.<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**парамстринг**</dt> </dl> | Указывает, что данные, связанные с ключом, являются строкой.<br/> |



 

</dd> <dt>

**\_Атрибуты P**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**\_Значение P**
</dt> <dd>

Указывает значение, связанное с параметром. Этот член является объединением [**\_ \_ значений params в службе RAS**](ras-params-value-str.md) . Если элемент **P \_ Type** имеет значение парамнумбер, то элемент **Number** в объединении содержит значения. Если **\_ тип P** — Парамстринг, то **строковый** элемент объединения содержит значение.

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

[Структуры администрирования сервера RAS](ras-server-administration-structures.md)
</dt> <dt>

[**расадминакцептневконнектион**](rasadminacceptnewconnection.md)
</dt> <dt>

[**расадминконнектионхангупнотификатион**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**расадминпортжетинфо**](rasadminportgetinfo.md)
</dt> </dl>

 

 





