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
# <a name="op_package_part-structure"></a><span data-ttu-id="289c3-103">Структура OP_PACKAGE_PART</span><span class="sxs-lookup"><span data-stu-id="289c3-103">OP_PACKAGE_PART structure</span></span>

<span data-ttu-id="289c3-104">Определяет структуру, содержащую набор данных, определяемый идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="289c3-104">Defines a structure that contains a data set identified by a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="289c3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="289c3-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a><span data-ttu-id="289c3-106">Члены</span><span class="sxs-lookup"><span data-stu-id="289c3-106">Members</span></span>

### <a name="parttype"></a><span data-ttu-id="289c3-107">парттипе</span><span class="sxs-lookup"><span data-stu-id="289c3-107">PartType</span></span>

<span data-ttu-id="289c3-108">Идентифицирует сериализованную структуру, содержащуюся в части, в следующей таблице:</span><span class="sxs-lookup"><span data-stu-id="289c3-108">Identifies the serialized structure contained in Part per the following table:</span></span>

|<span data-ttu-id="289c3-109">парттипе</span><span class="sxs-lookup"><span data-stu-id="289c3-109">PartType</span></span>|<span data-ttu-id="289c3-110">Значение</span><span class="sxs-lookup"><span data-stu-id="289c3-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="289c3-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span><span class="sxs-lookup"><span data-stu-id="289c3-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span></span>|<span data-ttu-id="289c3-112">Содержит сериализованную структуру ODJ_WIN7_BLOB.</span><span class="sxs-lookup"><span data-stu-id="289c3-112">Contains a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="289c3-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span><span class="sxs-lookup"><span data-stu-id="289c3-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span></span>|<span data-ttu-id="289c3-114">Содержит сериализованную структуру OP_JOIN_PROV2_PART.</span><span class="sxs-lookup"><span data-stu-id="289c3-114">Contains a serialized OP_JOIN_PROV2_PART structure.</span></span>|
|<span data-ttu-id="289c3-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span><span class="sxs-lookup"><span data-stu-id="289c3-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span></span>|<span data-ttu-id="289c3-116">Содержит сериализованную структуру OP_JOIN_PROV3_PART.</span><span class="sxs-lookup"><span data-stu-id="289c3-116">Contains a serialized OP_JOIN_PROV3_PART structure.</span></span>|
|<span data-ttu-id="289c3-117">GUID_CERT_PROVIDER {9c0971e9-832F-4873-8e87-ef1419d4781e}</span><span class="sxs-lookup"><span data-stu-id="289c3-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span></span>|<span data-ttu-id="289c3-118">Содержит сериализованную структуру OP_CERT_PART.</span><span class="sxs-lookup"><span data-stu-id="289c3-118">Contains a serialized OP_CERT_PART structure.</span></span>|
|<span data-ttu-id="289c3-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span><span class="sxs-lookup"><span data-stu-id="289c3-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span></span>|<span data-ttu-id="289c3-120">Содержит сериализованную структуру OP_POLICY_PART.</span><span class="sxs-lookup"><span data-stu-id="289c3-120">Contains a serialized OP_POLICY_PART structure.</span></span>|

### <a name="ulflags"></a><span data-ttu-id="289c3-121">улфлагс</span><span class="sxs-lookup"><span data-stu-id="289c3-121">ulFlags</span></span>

<span data-ttu-id="289c3-122">Необходимо задать ноль или более следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="289c3-122">Must be set to zero or more of the following flags:</span></span>

|<span data-ttu-id="289c3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="289c3-123">Value</span></span>|<span data-ttu-id="289c3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="289c3-124">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="289c3-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="289c3-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span></span>|<span data-ttu-id="289c3-126">Эта часть пакета считается важнейшей.</span><span class="sxs-lookup"><span data-stu-id="289c3-126">This package part is considered essential.</span></span> <span data-ttu-id="289c3-127">Если потребитель не распознает эту часть пакета или не может успешно обработать его, общая операция должна завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="289c3-127">If the consumer does not recognize this package part or fails to successfully process it, the overall operation must fail.</span></span>|

### <a name="part"></a><span data-ttu-id="289c3-128">Отделение</span><span class="sxs-lookup"><span data-stu-id="289c3-128">Part</span></span>

<span data-ttu-id="289c3-129">Содержит сериализованную структуру в структуре OP_BLOB.</span><span class="sxs-lookup"><span data-stu-id="289c3-129">Contains a serialized structure in an OP_BLOB structure.</span></span> <span data-ttu-id="289c3-130">Конкретная структура определяется Парттипе.</span><span class="sxs-lookup"><span data-stu-id="289c3-130">The specific structure is determined by PartType.</span></span>

### <a name="extension"></a><span data-ttu-id="289c3-131">Расширение</span><span class="sxs-lookup"><span data-stu-id="289c3-131">Extension</span></span>

<span data-ttu-id="289c3-132">Зарезервировано для будущего использования и должно иметь значение "все нули".</span><span class="sxs-lookup"><span data-stu-id="289c3-132">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="289c3-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="289c3-133">See also</span></span>

[<span data-ttu-id="289c3-134">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="289c3-134">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="289c3-135">**\_большой двоичный объект Op**</span><span class="sxs-lookup"><span data-stu-id="289c3-135">**OP\_BLOB**</span></span>](odj-op_blob.md)
