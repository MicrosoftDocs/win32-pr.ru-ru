---
description: ICE55 проверяет, что все объекты Локкпермиссион существуют и имеют допустимые значения разрешений.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265831"
---
# <a name="ice55"></a><span data-ttu-id="ef518-103">ICE55</span><span class="sxs-lookup"><span data-stu-id="ef518-103">ICE55</span></span>

<span data-ttu-id="ef518-104">ICE55 проверяет, что все объекты Локкпермиссион существуют и имеют допустимые значения разрешений.</span><span class="sxs-lookup"><span data-stu-id="ef518-104">ICE55 validates that all LockPermission objects exist and have valid permission values.</span></span>

## <a name="result"></a><span data-ttu-id="ef518-105">Результат</span><span class="sxs-lookup"><span data-stu-id="ef518-105">Result</span></span>

<span data-ttu-id="ef518-106">ICE55 сообщение об ошибке, если LockObject, указанный в [таблице локкпермиссионс](lockpermissions-table.md) , не существует или если в столбце разрешений не указан уровень привилегий.</span><span class="sxs-lookup"><span data-stu-id="ef518-106">ICE55 post an error if a LockObject listed in the [LockPermissions table](lockpermissions-table.md) does not exist or if no privilege level is specified in the Permission column.</span></span>

## <a name="example"></a><span data-ttu-id="ef518-107">Пример</span><span class="sxs-lookup"><span data-stu-id="ef518-107">Example</span></span>

<span data-ttu-id="ef518-108">ICE55 сообщит о следующих ошибках в примере.</span><span class="sxs-lookup"><span data-stu-id="ef518-108">ICE55 would report the following errors for the example.</span></span>

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

<span data-ttu-id="ef518-109">[Таблица локкпермиссионс](lockpermissions-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="ef518-109">[LockPermissions Table](lockpermissions-table.md) (partial)</span></span>



| <span data-ttu-id="ef518-110">LockObject</span><span class="sxs-lookup"><span data-stu-id="ef518-110">LockObject</span></span> | <span data-ttu-id="ef518-111">Таблица</span><span class="sxs-lookup"><span data-stu-id="ef518-111">Table</span></span> | <span data-ttu-id="ef518-112">Домен</span><span class="sxs-lookup"><span data-stu-id="ef518-112">Domain</span></span> | <span data-ttu-id="ef518-113">Пользователь</span><span class="sxs-lookup"><span data-stu-id="ef518-113">User</span></span>  | <span data-ttu-id="ef518-114">Разрешение</span><span class="sxs-lookup"><span data-stu-id="ef518-114">Permission</span></span> |
|------------|-------|--------|-------|------------|
| <span data-ttu-id="ef518-115">Файл1</span><span class="sxs-lookup"><span data-stu-id="ef518-115">File1</span></span>      | <span data-ttu-id="ef518-116">Файл</span><span class="sxs-lookup"><span data-stu-id="ef518-116">File</span></span>  |        | <span data-ttu-id="ef518-117">guest</span><span class="sxs-lookup"><span data-stu-id="ef518-117">guest</span></span> |            |
| <span data-ttu-id="ef518-118">Файл3</span><span class="sxs-lookup"><span data-stu-id="ef518-118">File3</span></span>      | <span data-ttu-id="ef518-119">Файл</span><span class="sxs-lookup"><span data-stu-id="ef518-119">File</span></span>  |        | <span data-ttu-id="ef518-120">guest</span><span class="sxs-lookup"><span data-stu-id="ef518-120">guest</span></span> | <span data-ttu-id="ef518-121">1</span><span class="sxs-lookup"><span data-stu-id="ef518-121">1</span></span>          |



 

<span data-ttu-id="ef518-122">[Таблица файлов](file-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="ef518-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="ef518-123">Файл</span><span class="sxs-lookup"><span data-stu-id="ef518-123">File</span></span>  | <span data-ttu-id="ef518-124">Версия</span><span class="sxs-lookup"><span data-stu-id="ef518-124">Version</span></span> | <span data-ttu-id="ef518-125">Язык</span><span class="sxs-lookup"><span data-stu-id="ef518-125">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="ef518-126">Файл1</span><span class="sxs-lookup"><span data-stu-id="ef518-126">File1</span></span> | <span data-ttu-id="ef518-127">Файл2</span><span class="sxs-lookup"><span data-stu-id="ef518-127">File2</span></span>   |          |
| <span data-ttu-id="ef518-128">Файл2</span><span class="sxs-lookup"><span data-stu-id="ef518-128">File2</span></span> | <span data-ttu-id="ef518-129">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="ef518-129">1.0.0.0</span></span> | <span data-ttu-id="ef518-130">1033</span><span class="sxs-lookup"><span data-stu-id="ef518-130">1033</span></span>     |



 

<span data-ttu-id="ef518-131">Объект file1 имеет значение NULL в столбце разрешений.</span><span class="sxs-lookup"><span data-stu-id="ef518-131">The object File1 has a null in the Permission column.</span></span> <span data-ttu-id="ef518-132">Каждая строка должна иметь значение в столбце permissions.</span><span class="sxs-lookup"><span data-stu-id="ef518-132">Each row must have a value in the Permissions column.</span></span> <span data-ttu-id="ef518-133">Чтобы устранить эту ошибку, укажите числовое значение в этом столбце.</span><span class="sxs-lookup"><span data-stu-id="ef518-133">To fix this error specify a numeric value in this column.</span></span> <span data-ttu-id="ef518-134">Если для этого объекта привилегии не требуются, следует удалить строку.</span><span class="sxs-lookup"><span data-stu-id="ef518-134">If no privileges are needed for this object then you should remove the row.</span></span>

<span data-ttu-id="ef518-135">Объект Файл3, описанный в таблице Локкпермиссионс, не перечислен в таблице File.</span><span class="sxs-lookup"><span data-stu-id="ef518-135">The object File3 described in the LockPermissions table is not listed in the File table.</span></span> <span data-ttu-id="ef518-136">Чтобы устранить эту ошибку, обратитесь к допустимому объекту.</span><span class="sxs-lookup"><span data-stu-id="ef518-136">To fix this error refer to a valid object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef518-137">См. также</span><span class="sxs-lookup"><span data-stu-id="ef518-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef518-138">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="ef518-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



