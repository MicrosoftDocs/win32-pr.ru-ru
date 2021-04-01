---
description: Содержит стандартный атрибут сведений. Этот атрибут имеется в каждой записи базового файла и должен быть резидентным.
ms.assetid: 8e668309-2722-4115-923d-bf0aa78d24f1
title: Структура STANDARD_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STANDARD_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4927553ac593475f8659932468227362ae19fe59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072337"
---
# <a name="standard_information-structure"></a><span data-ttu-id="570be-104">Стандартная \_ информационная структура</span><span class="sxs-lookup"><span data-stu-id="570be-104">STANDARD\_INFORMATION structure</span></span>

<span data-ttu-id="570be-105">\[Эта структура допустима только для томов NTFS версии 3; Он может быть изменен в будущих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="570be-105">\[This structure is valid only for version 3 of NTFS volumes; it may be altered in future versions.\]</span></span>

<span data-ttu-id="570be-106">Содержит стандартный атрибут сведений.</span><span class="sxs-lookup"><span data-stu-id="570be-106">Contains the standard information attribute.</span></span> <span data-ttu-id="570be-107">Этот атрибут имеется в каждой записи базового файла и должен быть резидентным.</span><span class="sxs-lookup"><span data-stu-id="570be-107">This attribute is present in every base file record and must be resident.</span></span>

## <a name="syntax"></a><span data-ttu-id="570be-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="570be-108">Syntax</span></span>


```C++
typedef struct _STANDARD_INFORMATION {
  UCHAR Reserved[0x30];
  ULONG OwnerId;
  ULONG SecurityId;
} STANDARD_INFORMATION, *PSTANDARD_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="570be-109">Члены</span><span class="sxs-lookup"><span data-stu-id="570be-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="570be-110">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="570be-110">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="570be-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="570be-111">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="570be-112">**OwnerId**</span><span class="sxs-lookup"><span data-stu-id="570be-112">**OwnerId**</span></span>
</dt> <dd>

<span data-ttu-id="570be-113">Идентификатор владельца файла из индекса безопасности.</span><span class="sxs-lookup"><span data-stu-id="570be-113">The identifier of the file owner, from the security index.</span></span>

</dd> <dt>

<span data-ttu-id="570be-114">**секуритид**</span><span class="sxs-lookup"><span data-stu-id="570be-114">**SecurityId**</span></span>
</dt> <dd>

<span data-ttu-id="570be-115">Идентификатор безопасности для файла.</span><span class="sxs-lookup"><span data-stu-id="570be-115">The security identifier for the file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="570be-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="570be-116">Remarks</span></span>

<span data-ttu-id="570be-117">Обратите внимание, что для этой структуры нет связанного файла заголовка.</span><span class="sxs-lookup"><span data-stu-id="570be-117">Note that there is no associated header file for this structure.</span></span>

<span data-ttu-id="570be-118">Это определение структуры допустимо только для основной версии 3 и дополнительной версии 0 или 1, как сообщается [**фсктл \_ Получение \_ \_ \_ данных тома NTFS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span><span class="sxs-lookup"><span data-stu-id="570be-118">This structure definition is valid only for major version 3 and minor version 0 or 1, as reported by [**FSCTL\_GET\_NTFS\_VOLUME\_DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_ntfs_volume_data).</span></span>

## <a name="see-also"></a><span data-ttu-id="570be-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="570be-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="570be-120">Основная таблица файлов</span><span class="sxs-lookup"><span data-stu-id="570be-120">Master File Table</span></span>](master-file-table.md)
</dt> </dl>

 

 
