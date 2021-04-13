---
title: OP_POLICY_ELEMENT
description: Определение OP_POLICY_ELEMENT IDL
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104339832"
---
# <a name="op_policy_element-structure"></a><span data-ttu-id="6c021-103">Структура OP_POLICY_ELEMENT</span><span class="sxs-lookup"><span data-stu-id="6c021-103">OP_POLICY_ELEMENT structure</span></span>

<span data-ttu-id="6c021-104">Определяет раздел реестра и имя значения, тип и значение, которые должны быть настроены в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="6c021-104">Defines a registry key and a value name, type, and value that should be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c021-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c021-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a><span data-ttu-id="6c021-106">Члены</span><span class="sxs-lookup"><span data-stu-id="6c021-106">Members</span></span>

### <a name="pkeypath"></a><span data-ttu-id="6c021-107">пкэйпас</span><span class="sxs-lookup"><span data-stu-id="6c021-107">pKeyPath</span></span>

<span data-ttu-id="6c021-108">Содержит путь к разделу реестра.</span><span class="sxs-lookup"><span data-stu-id="6c021-108">Contains the path of the registry key.</span></span>

### <a name="pvaluename"></a><span data-ttu-id="6c021-109">пвалуенаме</span><span class="sxs-lookup"><span data-stu-id="6c021-109">pValueName</span></span>

<span data-ttu-id="6c021-110">Содержит имя значения реестра.</span><span class="sxs-lookup"><span data-stu-id="6c021-110">Contains the name of the registry value.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="6c021-111">улвалуетипе</span><span class="sxs-lookup"><span data-stu-id="6c021-111">ulValueType</span></span>

<span data-ttu-id="6c021-112">Содержит одно из значений из [типов значений реестра](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="6c021-112">Contains one of the values from [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

### <a name="cbvaluedata"></a><span data-ttu-id="6c021-113">кбвалуедата</span><span class="sxs-lookup"><span data-stu-id="6c021-113">cbValueData</span></span>

<span data-ttu-id="6c021-114">Содержит размер Пвалуедата в байтах.</span><span class="sxs-lookup"><span data-stu-id="6c021-114">Contains the size of pValueData in bytes.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="6c021-115">улвалуетипе</span><span class="sxs-lookup"><span data-stu-id="6c021-115">ulValueType</span></span>

<span data-ttu-id="6c021-116">Содержит значение реестра.</span><span class="sxs-lookup"><span data-stu-id="6c021-116">Contains the value of the registry value.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c021-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c021-117">See also</span></span>

[<span data-ttu-id="6c021-118">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="6c021-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)