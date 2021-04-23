---
description: Содержит массив больших двоичных объектов.
ms.assetid: e87f493b-f160-4316-b369-75d20c735213
title: Структура BLOB_TABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BLOB_TABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 32bacc925381f1c7ed30aa66247671b67e31b7e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264372"
---
# <a name="blob_table-structure"></a><span data-ttu-id="c9896-103">Структура таблицы больших двоичных объектов \_</span><span class="sxs-lookup"><span data-stu-id="c9896-103">BLOB\_TABLE structure</span></span>

<span data-ttu-id="c9896-104">Структура **\_ таблицы больших двоичных объектов** содержит массив больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="c9896-104">The **BLOB\_TABLE** structure contains an array of BLOBs.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9896-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9896-105">Syntax</span></span>


```C++
typedef struct {
  DWORD dwNumBlobs;
  HBLOB hBlobs[];
} BLOB_TABLE, *PBLOB_TABLE;
```



## <a name="members"></a><span data-ttu-id="c9896-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c9896-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9896-107">**двнумблобс**</span><span class="sxs-lookup"><span data-stu-id="c9896-107">**dwNumBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="c9896-108">Индикатор, которым следуют многие большие двоичные объекты.</span><span class="sxs-lookup"><span data-stu-id="c9896-108">Indicator that many BLOBs follow.</span></span>

</dd> <dt>

<span data-ttu-id="c9896-109">**хблобс**</span><span class="sxs-lookup"><span data-stu-id="c9896-109">**hBlobs**</span></span>
</dt> <dd>

<span data-ttu-id="c9896-110">Обработчик для массива больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="c9896-110">Handle to the BLOB array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c9896-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c9896-111">Requirements</span></span>



| <span data-ttu-id="c9896-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c9896-112">Requirement</span></span> | <span data-ttu-id="c9896-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c9896-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c9896-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9896-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c9896-115">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c9896-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c9896-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9896-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c9896-117">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c9896-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c9896-118">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c9896-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9896-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9896-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




