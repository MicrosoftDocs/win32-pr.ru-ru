---
description: Содержит подписанный BLOB-объект.
ms.assetid: c12d9007-c779-4363-8e28-6387a665a0d6
title: Структура SIGNER_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CONTEXT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ebc7d5380438fc6cd28a43136273387c1919713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664387"
---
# <a name="signer_context-structure"></a><span data-ttu-id="efe44-103">\_Структура контекста подписывающий</span><span class="sxs-lookup"><span data-stu-id="efe44-103">SIGNER\_CONTEXT structure</span></span>

<span data-ttu-id="efe44-104">Структура **\_ контекста подписавшего** содержит подписанный [*большой двоичный объект*](../secgloss/b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="efe44-104">The **SIGNER\_CONTEXT** structure contains a signed [*BLOB*](../secgloss/b-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="efe44-105">Эта структура не определена ни в одном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="efe44-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="efe44-106">Чтобы использовать эту структуру, необходимо определить ее самостоятельно, как показано в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="efe44-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="efe44-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="efe44-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CONTEXT {
  DWORD cbSize;
  DWORD cbBlob;
  BYTE  *pbBlob;
} SIGNER_CONTEXT, *PSIGNER_CONTEXT;
```



## <a name="members"></a><span data-ttu-id="efe44-108">Члены</span><span class="sxs-lookup"><span data-stu-id="efe44-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="efe44-109">**кбсизе**</span><span class="sxs-lookup"><span data-stu-id="efe44-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="efe44-110">Размер структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="efe44-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="efe44-111">**кбблоб**</span><span class="sxs-lookup"><span data-stu-id="efe44-111">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="efe44-112">Размер (в байтах) элемента **пбблоб** .</span><span class="sxs-lookup"><span data-stu-id="efe44-112">The size, in bytes, of the **pbBlob** member.</span></span>

</dd> <dt>

<span data-ttu-id="efe44-113">**пбблоб**</span><span class="sxs-lookup"><span data-stu-id="efe44-113">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="efe44-114">Указатель на подписанный BLOB-объект.</span><span class="sxs-lookup"><span data-stu-id="efe44-114">A pointer to the signed BLOB.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="efe44-115">Требования</span><span class="sxs-lookup"><span data-stu-id="efe44-115">Requirements</span></span>



| <span data-ttu-id="efe44-116">Требование</span><span class="sxs-lookup"><span data-stu-id="efe44-116">Requirement</span></span> | <span data-ttu-id="efe44-117">Значение</span><span class="sxs-lookup"><span data-stu-id="efe44-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="efe44-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="efe44-118">Minimum supported client</span></span><br/> | <span data-ttu-id="efe44-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="efe44-119">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="efe44-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="efe44-120">Minimum supported server</span></span><br/> | <span data-ttu-id="efe44-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="efe44-121">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efe44-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="efe44-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe44-123">**сигнерсигн**</span><span class="sxs-lookup"><span data-stu-id="efe44-123">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="efe44-124">**сигнерсигнекс**</span><span class="sxs-lookup"><span data-stu-id="efe44-124">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
