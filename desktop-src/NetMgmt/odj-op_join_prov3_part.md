---
title: OP_JOINPROV3_PART
description: Определение OP_JOINPROV3_PART IDL
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104414040"
---
# <a name="op_joinprov3_part-structure"></a><span data-ttu-id="33eb0-103">Структура OP_JOINPROV3_PART</span><span class="sxs-lookup"><span data-stu-id="33eb0-103">OP_JOINPROV3_PART structure</span></span>

<span data-ttu-id="33eb0-104">Содержит дополнительные сведения, используемые для настройки клиента, присоединяемого к домену.</span><span class="sxs-lookup"><span data-stu-id="33eb0-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="33eb0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33eb0-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a><span data-ttu-id="33eb0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="33eb0-106">Members</span></span>

### <a name="rid"></a><span data-ttu-id="33eb0-107">Избежать</span><span class="sxs-lookup"><span data-stu-id="33eb0-107">Rid</span></span>

<span data-ttu-id="33eb0-108">Необходимо задать относительный идентификатор SID учетной записи компьютера</span><span class="sxs-lookup"><span data-stu-id="33eb0-108">Must be set to the Relative Identifier of the machine account’s SID</span></span>

### <a name="lpsid"></a><span data-ttu-id="33eb0-109">лпсид</span><span class="sxs-lookup"><span data-stu-id="33eb0-109">lpSid</span></span>

<span data-ttu-id="33eb0-110">Необходимо задать идентификатор безопасности учетной записи компьютера в виде строки.</span><span class="sxs-lookup"><span data-stu-id="33eb0-110">Must be set to the SID of the machine account in string form.</span></span>

## <a name="see-also"></a><span data-ttu-id="33eb0-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33eb0-111">See also</span></span>

[<span data-ttu-id="33eb0-112">**Определения IDL для автономного присоединение к домену**</span><span class="sxs-lookup"><span data-stu-id="33eb0-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
