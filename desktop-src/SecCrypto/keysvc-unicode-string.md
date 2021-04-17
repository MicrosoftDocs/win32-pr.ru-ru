---
description: '\_ \_ Структура строки Юникода кэйсвк определяет строку в Юникоде и максимальную длину строки. Эта структура используется функцией Ркэйпфксинсталл.'
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: Структура KEYSVC_UNICODE_STRING (Ркэйсвкк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684578"
---
# <a name="keysvc_unicode_string-structure"></a><span data-ttu-id="57935-104">КЭЙСВК \_ \_ строковая структура Юникода</span><span class="sxs-lookup"><span data-stu-id="57935-104">KEYSVC\_UNICODE\_STRING structure</span></span>

<span data-ttu-id="57935-105">Структура **\_ \_ строки Юникода кэйсвк** определяет строку в [*Юникоде*](../secgloss/u-gly.md) и максимальную длину строки.</span><span class="sxs-lookup"><span data-stu-id="57935-105">The **KEYSVC\_UNICODE\_STRING** structure defines a [*Unicode*](../secgloss/u-gly.md) string and a maximum length for the string.</span></span> <span data-ttu-id="57935-106">Эта структура используется функцией [**ркэйпфксинсталл**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="57935-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="57935-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57935-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a><span data-ttu-id="57935-108">Члены</span><span class="sxs-lookup"><span data-stu-id="57935-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="57935-109">**Длина**</span><span class="sxs-lookup"><span data-stu-id="57935-109">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="57935-110">Значение **UShort** , указывающее длину в байтах, используемую для **buffer**.</span><span class="sxs-lookup"><span data-stu-id="57935-110">A **USHORT** value that specifies the length, in bytes, used for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="57935-111">**MaximumLength**</span><span class="sxs-lookup"><span data-stu-id="57935-111">**MaximumLength**</span></span>
</dt> <dd>

<span data-ttu-id="57935-112">Значение **UShort** , указывающее максимальную длину в байтах, допустимую для **buffer**.</span><span class="sxs-lookup"><span data-stu-id="57935-112">A **USHORT** value that specifies the maximum length, in bytes, allowed for **Buffer**.</span></span>

</dd> <dt>

<span data-ttu-id="57935-113">**Буфер**</span><span class="sxs-lookup"><span data-stu-id="57935-113">**Buffer**</span></span>
</dt> <dd>

<span data-ttu-id="57935-114">Указатель на **UShort** , представляющий строку в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="57935-114">A pointer to a **USHORT** that represents the Unicode string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57935-115">Требования</span><span class="sxs-lookup"><span data-stu-id="57935-115">Requirements</span></span>



| <span data-ttu-id="57935-116">Требование</span><span class="sxs-lookup"><span data-stu-id="57935-116">Requirement</span></span> | <span data-ttu-id="57935-117">Значение</span><span class="sxs-lookup"><span data-stu-id="57935-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57935-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57935-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57935-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="57935-119">None supported</span></span><br/>                                                             |
| <span data-ttu-id="57935-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57935-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57935-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="57935-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57935-122">Header</span><span class="sxs-lookup"><span data-stu-id="57935-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="57935-123"><dt>Ркэйсвкк. h</dt></span><span class="sxs-lookup"><span data-stu-id="57935-123"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57935-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57935-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57935-125">**ркэйпфксинсталл**</span><span class="sxs-lookup"><span data-stu-id="57935-125">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="57935-126">**\_большой двоичный объект кэйсвк**</span><span class="sxs-lookup"><span data-stu-id="57935-126">**KEYSVC\_BLOB**</span></span>](keysvc-blob.md)
</dt> </dl>

 

 
