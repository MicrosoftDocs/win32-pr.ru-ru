---
description: Содержит сведения о выбранном файле в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).
title: Структура FMS_GETFILESEL (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990831"
---
# <a name="fms_getfilesel-structure"></a><span data-ttu-id="eb967-103">\_Структура FMS жетфилесел</span><span class="sxs-lookup"><span data-stu-id="eb967-103">FMS\_GETFILESEL structure</span></span>

<span data-ttu-id="eb967-104">Содержит сведения о выбранном файле в активном окне диспетчера файлов (в окне каталога или в окне результатов поиска).</span><span class="sxs-lookup"><span data-stu-id="eb967-104">Contains information about a selected file in the active File Manager window (the directory window or the Search Results window).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb967-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb967-105">Syntax</span></span>


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a><span data-ttu-id="eb967-106">Участники</span><span class="sxs-lookup"><span data-stu-id="eb967-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="eb967-107">**фттиме**</span><span class="sxs-lookup"><span data-stu-id="eb967-107">**ftTime**</span></span>
</dt> <dd>

<span data-ttu-id="eb967-108">Тип: **fileTime**</span><span class="sxs-lookup"><span data-stu-id="eb967-108">Type: **FILETIME**</span></span>

</dd> <dd>

<span data-ttu-id="eb967-109">Дата и время создания файла.</span><span class="sxs-lookup"><span data-stu-id="eb967-109">The time and date the file was created.</span></span>

</dd> <dt>

<span data-ttu-id="eb967-110">**двсизе**</span><span class="sxs-lookup"><span data-stu-id="eb967-110">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="eb967-111">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="eb967-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="eb967-112">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="eb967-112">The size, in bytes, of the file.</span></span>

</dd> <dt>

<span data-ttu-id="eb967-113">**баттр**</span><span class="sxs-lookup"><span data-stu-id="eb967-113">**bAttr**</span></span>
</dt> <dd>

<span data-ttu-id="eb967-114">Тип: **Byte**</span><span class="sxs-lookup"><span data-stu-id="eb967-114">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="eb967-115">Атрибуты файла.</span><span class="sxs-lookup"><span data-stu-id="eb967-115">The attributes of the file.</span></span>

</dd> <dt>

<span data-ttu-id="eb967-116">**szName**</span><span class="sxs-lookup"><span data-stu-id="eb967-116">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="eb967-117">Тип: **TCHAR**</span><span class="sxs-lookup"><span data-stu-id="eb967-117">Type: **TCHAR**</span></span>

</dd> <dd>

<span data-ttu-id="eb967-118">Полный путь и имя файла выбранного файла, заканчивающиеся нулем.</span><span class="sxs-lookup"><span data-stu-id="eb967-118">The null-terminated full path and file name of the selected file.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb967-119">Требования</span><span class="sxs-lookup"><span data-stu-id="eb967-119">Requirements</span></span>



| <span data-ttu-id="eb967-120">Требование</span><span class="sxs-lookup"><span data-stu-id="eb967-120">Requirement</span></span> | <span data-ttu-id="eb967-121">Значение</span><span class="sxs-lookup"><span data-stu-id="eb967-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb967-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb967-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eb967-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="eb967-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="eb967-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb967-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eb967-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="eb967-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eb967-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="eb967-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb967-127"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb967-127"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb967-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb967-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb967-129">**фмекстенсионпрок**</span><span class="sxs-lookup"><span data-stu-id="eb967-129">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




