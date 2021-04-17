---
title: Перечисление BITS_FILE_PROPERTY_ID (Deliveryoptimization. h)
description: В перечислении BITS_FILE_PROPERTY_ID указываются значения, определяющие значения ИДЕНТИФИКАТОРов, соответствующие свойствам Баккграундкопифиле.
ms.assetid: 47EFD160-7CA8-48E6-A18E-38D85F7C6E47
keywords:
- Перечисление BITS_FILE_PROPERTY_ID
- Перечисление BITS_FILE_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b6c6b8a4de359e8313e3127080f2cc17ae6478c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710476"
---
# <a name="bits_file_property_id-enumeration"></a>Перечисление BITS_FILE_PROPERTY_ID

В перечислении **BITS_FILE_PROPERTY_ID** указываются значения, определяющие значения идентификаторов, соответствующие свойствам **баккграундкопифиле** .

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _BITS_FILE_PROPERTY_ID { 
  BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS  = 1
} BITS_FILE_PROPERTY_ID;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS"></span><span id="bits_file_property_id_http_response_headers"></span>**BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**
</dt> <dd>

Полный набор HTTP-заголовков ответа из последнего HTTP-пакета ответа сервера.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





