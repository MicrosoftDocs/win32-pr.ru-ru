---
description: Свойство FileAttributes объекта Installer возвращает число, представляющее комбинированные атрибуты файла для указанного пути к файлу или папке.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Свойство установщика. FileAttributes (Windows. Storage. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651609"
---
# <a name="installerfileattributes-property"></a><span data-ttu-id="36615-103">Свойство Installer. FileAttributes</span><span class="sxs-lookup"><span data-stu-id="36615-103">Installer.FileAttributes property</span></span>

<span data-ttu-id="36615-104">Свойство **FileAttributes** объекта [**Installer**](installer-object.md) возвращает число, представляющее комбинированные атрибуты файла для указанного пути к файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="36615-104">The **FileAttributes** property of the [**Installer**](installer-object.md) object returns a number representing the combined file attributes for the designated path to a file or folder.</span></span>

<span data-ttu-id="36615-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="36615-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="36615-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36615-106">Syntax</span></span>


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a><span data-ttu-id="36615-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="36615-107">Property value</span></span>

<span data-ttu-id="36615-108">Требуемый путь к файлу или папке.</span><span class="sxs-lookup"><span data-stu-id="36615-108">The required path to the file or folder.</span></span> <span data-ttu-id="36615-109">Частичный путь предполагает наличие текущего каталога.</span><span class="sxs-lookup"><span data-stu-id="36615-109">A partial path assumes the current directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="36615-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36615-110">Remarks</span></span>

<span data-ttu-id="36615-111">Свойство **FileAttributes** возвращает следующие значения.</span><span class="sxs-lookup"><span data-stu-id="36615-111">The **FileAttributes** property returns the following values.</span></span>



| <span data-ttu-id="36615-112">Атрибут файла</span><span class="sxs-lookup"><span data-stu-id="36615-112">File attribute</span></span>              | <span data-ttu-id="36615-113">Значение</span><span class="sxs-lookup"><span data-stu-id="36615-113">Value</span></span>      | <span data-ttu-id="36615-114">Значение</span><span class="sxs-lookup"><span data-stu-id="36615-114">Value</span></span> |
|-----------------------------|------------|-------|
| <span data-ttu-id="36615-115">FILE\_ATTRIBUTE\_READONLY</span><span class="sxs-lookup"><span data-stu-id="36615-115">FILE\_ATTRIBUTE\_READONLY</span></span>   | <span data-ttu-id="36615-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="36615-116">0x00000001</span></span> | <span data-ttu-id="36615-117">1</span><span class="sxs-lookup"><span data-stu-id="36615-117">1</span></span>     |
| <span data-ttu-id="36615-118">FILE\_ATTRIBUTE\_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="36615-118">FILE\_ATTRIBUTE\_HIDDEN</span></span>     | <span data-ttu-id="36615-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="36615-119">0x00000002</span></span> | <span data-ttu-id="36615-120">2</span><span class="sxs-lookup"><span data-stu-id="36615-120">2</span></span>     |
| <span data-ttu-id="36615-121">FILE\_ATTRIBUTE\_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="36615-121">FILE\_ATTRIBUTE\_SYSTEM</span></span>     | <span data-ttu-id="36615-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="36615-122">0x00000004</span></span> | <span data-ttu-id="36615-123">4</span><span class="sxs-lookup"><span data-stu-id="36615-123">4</span></span>     |
| <span data-ttu-id="36615-124">FILE\_ATTRIBUTE\_DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="36615-124">FILE\_ATTRIBUTE\_DIRECTORY</span></span>  | <span data-ttu-id="36615-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="36615-125">0x00000010</span></span> | <span data-ttu-id="36615-126">16</span><span class="sxs-lookup"><span data-stu-id="36615-126">16</span></span>    |
| <span data-ttu-id="36615-127">\_ \_ временный атрибут файла</span><span class="sxs-lookup"><span data-stu-id="36615-127">FILE\_ATTRIBUTE\_TEMPORARY</span></span>  | <span data-ttu-id="36615-128">0x00000100</span><span class="sxs-lookup"><span data-stu-id="36615-128">0x00000100</span></span> | <span data-ttu-id="36615-129">256</span><span class="sxs-lookup"><span data-stu-id="36615-129">256</span></span>   |
| <span data-ttu-id="36615-130">FILE\_ATTRIBUTE\_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="36615-130">FILE\_ATTRIBUTE\_COMPRESSED</span></span> | <span data-ttu-id="36615-131">0x00000800</span><span class="sxs-lookup"><span data-stu-id="36615-131">0x00000800</span></span> | <span data-ttu-id="36615-132">2048</span><span class="sxs-lookup"><span data-stu-id="36615-132">2048</span></span>  |
| <span data-ttu-id="36615-133">FILE\_ATTRIBUTE\_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="36615-133">FILE\_ATTRIBUTE\_OFFLINE</span></span>    | <span data-ttu-id="36615-134">0x00001000</span><span class="sxs-lookup"><span data-stu-id="36615-134">0x00001000</span></span> | <span data-ttu-id="36615-135">4096</span><span class="sxs-lookup"><span data-stu-id="36615-135">4096</span></span>  |



 

<span data-ttu-id="36615-136">Возвращает значение – 1, если файл или папка не существуют или недоступны.</span><span class="sxs-lookup"><span data-stu-id="36615-136">Returns –1 if the file or folder does not exist or is not accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="36615-137">Требования</span><span class="sxs-lookup"><span data-stu-id="36615-137">Requirements</span></span>



| <span data-ttu-id="36615-138">Требование</span><span class="sxs-lookup"><span data-stu-id="36615-138">Requirement</span></span> | <span data-ttu-id="36615-139">Значение</span><span class="sxs-lookup"><span data-stu-id="36615-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36615-140">Версия</span><span class="sxs-lookup"><span data-stu-id="36615-140">Version</span></span><br/> | <span data-ttu-id="36615-141">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="36615-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="36615-142">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="36615-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="36615-143">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="36615-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="36615-144">Header</span><span class="sxs-lookup"><span data-stu-id="36615-144">Header</span></span><br/>  | <dl> <span data-ttu-id="36615-145"><dt>Windows. Storage. h</dt></span><span class="sxs-lookup"><span data-stu-id="36615-145"><dt>Windows.storage.h</dt></span></span> </dl>                                                                                                                                                            |
| <span data-ttu-id="36615-146">DLL</span><span class="sxs-lookup"><span data-stu-id="36615-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="36615-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36615-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="36615-148">IID</span><span class="sxs-lookup"><span data-stu-id="36615-148">IID</span></span><br/>     | <span data-ttu-id="36615-149">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="36615-149">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




