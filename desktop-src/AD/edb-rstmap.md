---
title: Структура EDB_RSTMAP (Нтдсбкли. h)
description: Используется с функцией Дсресторерегистер для преобразования резервной копии базы данных в новую базу данных.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP структуры Active Directory
- PEDB_RSTMAP Active Directory указателя на структуру
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071741"
---
# <a name="edb_rstmap-structure"></a><span data-ttu-id="8972b-105">\_Структура EDB рстмап</span><span class="sxs-lookup"><span data-stu-id="8972b-105">EDB\_RSTMAP structure</span></span>

<span data-ttu-id="8972b-106">Структура **EDB \_ рстмап** используется с функцией [**дсресторерегистер**](dsrestoreregister.md) для отображения резервной копии базы данных в новой базе данных.</span><span class="sxs-lookup"><span data-stu-id="8972b-106">The **EDB\_RSTMAP** structure is used with the [**DsRestoreRegister**](dsrestoreregister.md) function to map a backed up database to a new database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8972b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8972b-107">Syntax</span></span>


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a><span data-ttu-id="8972b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="8972b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8972b-109">**сздатабасенаме**</span><span class="sxs-lookup"><span data-stu-id="8972b-109">**szDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="8972b-110">Указатель на строку, завершающуюся нулем, которая содержит имя базы данных при ее резервном копировании.</span><span class="sxs-lookup"><span data-stu-id="8972b-110">Pointer to a null-terminated string that contains the name of the database when it was backed up.</span></span>

</dd> <dt>

<span data-ttu-id="8972b-111">**сзневдатабасенаме**</span><span class="sxs-lookup"><span data-stu-id="8972b-111">**szNewDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="8972b-112">Указатель на строку, завершающуюся нулем, которая содержит новое имя базы данных, включая ее новое расположение, если применимо.</span><span class="sxs-lookup"><span data-stu-id="8972b-112">Pointer to a null-terminated string that contains the new name of the database, including its new location, when applicable.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8972b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8972b-113">Requirements</span></span>



| <span data-ttu-id="8972b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8972b-114">Requirement</span></span> | <span data-ttu-id="8972b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8972b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8972b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8972b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8972b-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8972b-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="8972b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8972b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8972b-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8972b-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="8972b-120">Header</span><span class="sxs-lookup"><span data-stu-id="8972b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8972b-121"><dt>Нтдсбкли. h</dt></span><span class="sxs-lookup"><span data-stu-id="8972b-121"><dt>Ntdsbcli.h</dt></span></span> </dl> |
| <span data-ttu-id="8972b-122">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8972b-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8972b-123">**EDB \_ РСТМАПВ** (Юникод) и **\_ рстмапа EDB** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8972b-123">**EDB\_RSTMAPW** (Unicode) and **EDB\_RSTMAPA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="8972b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8972b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8972b-125">**дсресторерегистер**</span><span class="sxs-lookup"><span data-stu-id="8972b-125">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="8972b-126">Структуры резервного копирования каталога</span><span class="sxs-lookup"><span data-stu-id="8972b-126">Directory Backup Structures</span></span>](directory-backup-structures.md)
</dt> </dl>

 

 





