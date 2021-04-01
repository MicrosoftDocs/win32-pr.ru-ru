---
title: OP_PACKAGE_PART
description: Определение OP_PACKAGE_PART IDL
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104261555"
---
# <a name="op_package_part-structure"></a>Структура OP_PACKAGE_PART

Определяет структуру, содержащую набор данных, определяемый идентификатором GUID.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a>Члены

### <a name="parttype"></a>парттипе

Идентифицирует сериализованную структуру, содержащуюся в части, в следующей таблице:

|парттипе|Значение|
| --- | --- |
|GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}|Содержит сериализованную структуру ODJ_WIN7_BLOB.|
|GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}|Содержит сериализованную структуру OP_JOIN_PROV2_PART.|
|GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}|Содержит сериализованную структуру OP_JOIN_PROV3_PART.|
|GUID_CERT_PROVIDER {9c0971e9-832F-4873-8e87-ef1419d4781e}|Содержит сериализованную структуру OP_CERT_PART.|
|GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}|Содержит сериализованную структуру OP_POLICY_PART.|

### <a name="ulflags"></a>улфлагс

Необходимо задать ноль или более следующих флагов:

|Значение|Значение|
| --- | --- |
|OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)|Эта часть пакета считается важнейшей. Если потребитель не распознает эту часть пакета или не может успешно обработать его, общая операция должна завершиться ошибкой.|

### <a name="part"></a>Отделение

Содержит сериализованную структуру в структуре OP_BLOB. Конкретная структура определяется Парттипе.

### <a name="extension"></a>Расширение

Зарезервировано для будущего использования и должно иметь значение "все нули".

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

[**\_большой двоичный объект Op**](odj-op_blob.md)
