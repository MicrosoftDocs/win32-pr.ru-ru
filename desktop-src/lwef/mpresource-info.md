---
title: Структура MPRESOURCE_INFO (Мпклиент. h)
description: Структура сведений о ресурсах.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO структуры устаревшие функции среды Windows
- Функции PMPRESOURCE_INFO указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988923"
---
# <a name="mpresource_info-structure"></a>\_Структура сведений о мпресаурце

Структура сведений о ресурсах.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**Схема**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Идентификатор схемы ресурсов, например "File" или "Dir".

</dd> <dt>

**Путь**
</dt> <dd>

Тип: **\_ \_ строка MP MIDL, LPWSTR**

</dd> <dd>

Абсолютный путь к ресурсу на основе **схемы**.

</dd> <dt>

**Класс**
</dt> <dd>

Тип: **\_ класс мпресаурце**

</dd> <dd>

Это поле задается, когда ресурс идентифицируется как часть угрозы. Он указывает класс ресурсов, в основном и нескрытое. Это может быть сочетание следующих возможных значений:



| Значение                                                                                                                                                                                                                                                                        | Значение                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <dt>**Пакет управления \_ \_Неизвестный \_ символ 0X0000 класса ресурсов**</dt> <dt></dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <dt>**Пакет управления \_ \_Класс ресурсов \_ бетон**</dt> <dt>0x0001</dt> </dl>           | Взаимоисключающий с **\_ \_ классом \_ ресурсов MP "скрытые**".<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <dt>**Пакет управления \_ Класс ресурсов — \_ \_ скрытые**</dt> <dt>0x0002</dt> </dl>                 | Взаимоисключающий с **\_ \_ \_ конкретным классом ресурсов MP**.<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <dt>**Пакет управления \_ \_ \_ Пример \_ файла 0x0004 класса ресурсов**</dt> <dt></dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <dt>**Пакет управления \_ \_Класс ресурсов \_ Shared**</dt> <dt>0x0100</dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





