---
title: Структура MPCOMPONENT_VERSION (Мпклиент. h)
description: Версия и время обновления отдельного компонента.
ms.assetid: 43468230-EE13-4630-8C09-F8DF983EF748
keywords:
- MPCOMPONENT_VERSION структуры устаревшие функции среды Windows
- Функции PMPCOMPONENT_VERSION указателя структур в устаревшей среде Windows
topic_type:
- apiref
api_name:
- MPCOMPONENT_VERSION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a1d4b5011bb185dc8ca0892e0a0e65bc4a7d8b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988601"
---
# <a name="mpcomponent_version-structure"></a><span data-ttu-id="d22c0-105">\_Структура версии мпкомпонент</span><span class="sxs-lookup"><span data-stu-id="d22c0-105">MPCOMPONENT\_VERSION structure</span></span>

<span data-ttu-id="d22c0-106">Версия и время обновления отдельного компонента.</span><span class="sxs-lookup"><span data-stu-id="d22c0-106">Version and update time for an individual component.</span></span>

## <a name="syntax"></a><span data-ttu-id="d22c0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d22c0-107">Syntax</span></span>


```C++
typedef struct tagMPCOMPONENT_VERSION {
  ULONGLONG      Version;
  ULARGE_INTEGER UpdateTime;
} MPCOMPONENT_VERSION, *PMPCOMPONENT_VERSION;
```



## <a name="members"></a><span data-ttu-id="d22c0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="d22c0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d22c0-109">**Version**</span><span class="sxs-lookup"><span data-stu-id="d22c0-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="d22c0-110">Тип: **улонглонг**</span><span class="sxs-lookup"><span data-stu-id="d22c0-110">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="d22c0-111">Поле версии.</span><span class="sxs-lookup"><span data-stu-id="d22c0-111">Version field.</span></span> <span data-ttu-id="d22c0-112">Каждое **слово** представляет основную, дополнительную, сборку и редакцию.</span><span class="sxs-lookup"><span data-stu-id="d22c0-112">Each **WORD** represents major, minor, build, and revision.</span></span>

</dd> <dt>

<span data-ttu-id="d22c0-113">**UpdateTime**</span><span class="sxs-lookup"><span data-stu-id="d22c0-113">**UpdateTime**</span></span>
</dt> <dd>

<span data-ttu-id="d22c0-114">Тип: **уларже \_ Integer**</span><span class="sxs-lookup"><span data-stu-id="d22c0-114">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="d22c0-115">Время последнего обновления компонента в формате **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="d22c0-115">Last update time of the component, in **FILETIME** format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d22c0-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d22c0-116">Requirements</span></span>



| <span data-ttu-id="d22c0-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d22c0-117">Requirement</span></span> | <span data-ttu-id="d22c0-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d22c0-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d22c0-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d22c0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d22c0-120">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d22c0-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d22c0-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d22c0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d22c0-122">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d22c0-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d22c0-123">Header</span><span class="sxs-lookup"><span data-stu-id="d22c0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d22c0-124"><dt>Мпклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="d22c0-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





