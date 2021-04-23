---
description: Указывает, какие байты зашифрованы в защищенной видеоповерхности.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: Структура D3DENCRYPTED_BLOCK_INFO (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143153"
---
# <a name="d3dencrypted_block_info-structure"></a><span data-ttu-id="ba297-103">\_ \_ Структура сведений о БЛОКе D3DENCRYPTED</span><span class="sxs-lookup"><span data-stu-id="ba297-103">D3DENCRYPTED\_BLOCK\_INFO structure</span></span>

<span data-ttu-id="ba297-104">Указывает, какие байты зашифрованы в защищенной видеоповерхности.</span><span class="sxs-lookup"><span data-stu-id="ba297-104">Specifies which bytes are encrypted in a protected video surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba297-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba297-105">Syntax</span></span>


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a><span data-ttu-id="ba297-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ba297-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba297-107">**нуменкриптедбитесатбегиннинг**</span><span class="sxs-lookup"><span data-stu-id="ba297-107">**NumEncryptedBytesAtBeginning**</span></span>
</dt> <dd>

<span data-ttu-id="ba297-108">Число байтов, зашифрованных в начале буфера.</span><span class="sxs-lookup"><span data-stu-id="ba297-108">The number of bytes that are encrypted at the start of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ba297-109">**нумбитесинскиппаттерн**</span><span class="sxs-lookup"><span data-stu-id="ba297-109">**NumBytesInSkipPattern**</span></span>
</dt> <dd>

<span data-ttu-id="ba297-110">Число байтов, пропущенных после первого **нуменкриптедбитесатбегиннинг** байт, а затем после каждого блока **нумбитесиненкриптпаттерн** байт.</span><span class="sxs-lookup"><span data-stu-id="ba297-110">The number of bytes that are skipped after the first **NumEncryptedBytesAtBeginning** bytes, and then after each block of **NumBytesInEncryptPattern** bytes.</span></span> <span data-ttu-id="ba297-111">Пропущенные байты не шифруются.</span><span class="sxs-lookup"><span data-stu-id="ba297-111">Skipped bytes are not encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="ba297-112">**нумбитесиненкриптпаттерн**</span><span class="sxs-lookup"><span data-stu-id="ba297-112">**NumBytesInEncryptPattern**</span></span>
</dt> <dd>

<span data-ttu-id="ba297-113">Число байтов, зашифрованных после каждого блока пропущенных байтов.</span><span class="sxs-lookup"><span data-stu-id="ba297-113">The number of bytes that are encrypted after each block of skipped bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba297-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ba297-114">Requirements</span></span>



| <span data-ttu-id="ba297-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ba297-115">Requirement</span></span> | <span data-ttu-id="ba297-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ba297-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba297-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba297-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ba297-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ba297-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ba297-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba297-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ba297-120">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba297-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ba297-121">Header</span><span class="sxs-lookup"><span data-stu-id="ba297-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba297-122"><dt>D3d9types. h (включение D3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba297-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba297-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba297-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba297-124">Видеоструктуры Direct3D</span><span class="sxs-lookup"><span data-stu-id="ba297-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




