---
description: '\_Структура больших двоичных объектов кэйсвк определяет большой двоичный объект службы Key. Эта структура используется функцией Ркэйпфксинсталл.'
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: Структура KEYSVC_BLOB (Ркэйсвкк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664627"
---
# <a name="keysvc_blob-structure"></a><span data-ttu-id="fb736-104">\_Структура больших двоичных объектов кэйсвк</span><span class="sxs-lookup"><span data-stu-id="fb736-104">KEYSVC\_BLOB structure</span></span>

<span data-ttu-id="fb736-105">Структура **\_ больших двоичных объектов кэйсвк** определяет большой двоичный объект службы Key.</span><span class="sxs-lookup"><span data-stu-id="fb736-105">The **KEYSVC\_BLOB** structure defines a key service BLOB.</span></span> <span data-ttu-id="fb736-106">Эта структура используется функцией [**ркэйпфксинсталл**](rkeypfxinstall.md) .</span><span class="sxs-lookup"><span data-stu-id="fb736-106">This structure is used by the [**RKeyPFXInstall**](rkeypfxinstall.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb736-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb736-107">Syntax</span></span>


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a><span data-ttu-id="fb736-108">Члены</span><span class="sxs-lookup"><span data-stu-id="fb736-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fb736-109">**CB**</span><span class="sxs-lookup"><span data-stu-id="fb736-109">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="fb736-110">Значение типа **ulong** , указывающее размер в байтах, который равен **Pb**.</span><span class="sxs-lookup"><span data-stu-id="fb736-110">A **ULONG** value that specifies the size, in bytes, of **pb**.</span></span>

</dd> <dt>

<span data-ttu-id="fb736-111">**МС**</span><span class="sxs-lookup"><span data-stu-id="fb736-111">**pb**</span></span>
</dt> <dd>

<span data-ttu-id="fb736-112">Указатель на **байт** , содержащий большой двоичный объект, в формате [*PKCS \# 12*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="fb736-112">A pointer to a **BYTE** that contains the BLOB, in [*PKCS \#12*](../secgloss/p-gly.md) format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb736-113">Требования</span><span class="sxs-lookup"><span data-stu-id="fb736-113">Requirements</span></span>



| <span data-ttu-id="fb736-114">Требование</span><span class="sxs-lookup"><span data-stu-id="fb736-114">Requirement</span></span> | <span data-ttu-id="fb736-115">Значение</span><span class="sxs-lookup"><span data-stu-id="fb736-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb736-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb736-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fb736-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fb736-117">None supported</span></span><br/>                                                             |
| <span data-ttu-id="fb736-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb736-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fb736-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb736-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fb736-120">Header</span><span class="sxs-lookup"><span data-stu-id="fb736-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb736-121"><dt>Ркэйсвкк. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb736-121"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb736-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb736-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb736-123">**ркэйпфксинсталл**</span><span class="sxs-lookup"><span data-stu-id="fb736-123">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> <dt>

[<span data-ttu-id="fb736-124">**\_строка Юникода \_ кэйсвк**</span><span class="sxs-lookup"><span data-stu-id="fb736-124">**KEYSVC\_UNICODE\_STRING**</span></span>](keysvc-unicode-string.md)
</dt> </dl>

 

 
