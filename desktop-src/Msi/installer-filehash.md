---
description: Метод FileHash объекта Installer принимает путь к файлу и возвращает 128-разрядный хэш этого файла. Сведения о хэш-файле возвращаются в виде объекта записи. Весь 128-разрядный хэш-файл возвращается в виде полей свойств 4 32-bit IntegerData.
ms.assetid: 065ffde1-4d7c-4e71-9315-7926d4cd38ed
title: Метод Installer. FileHash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileHash
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a38ef741c5c3a33c526cc78fbdc4551716ed3ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651608"
---
# <a name="installerfilehash-method"></a><span data-ttu-id="d0f49-105">Метод Installer. FileHash</span><span class="sxs-lookup"><span data-stu-id="d0f49-105">Installer.FileHash method</span></span>

<span data-ttu-id="d0f49-106">Метод **FileHash** [**объекта Installer**](installer-object.md) принимает путь к файлу и возвращает 128-разрядный хэш этого файла.</span><span class="sxs-lookup"><span data-stu-id="d0f49-106">The **FileHash** method of the [**Installer Object**](installer-object.md) takes the path to a file and returns a 128-bit hash of that file.</span></span> <span data-ttu-id="d0f49-107">Сведения о хэш-файле возвращаются в виде [**объекта записи**](record-object.md).</span><span class="sxs-lookup"><span data-stu-id="d0f49-107">The file hash information is returned as a [**Record Object**](record-object.md).</span></span> <span data-ttu-id="d0f49-108">Весь 128-разрядный хэш-файл возвращается в виде полей свойств 4 32-bit [**IntegerData**](record-integerdata.md) .</span><span class="sxs-lookup"><span data-stu-id="d0f49-108">The entire 128-bit file hash is returned as four 32-bit [**IntegerData**](record-integerdata.md) property fields.</span></span>

<span data-ttu-id="d0f49-109">Значения, возвращаемые в [**объекте Record**](record-object.md) , соответствуют четырем полям структуры [**мсифилехашинфо**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) , возвращаемой [**мсижетфилехаш**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span><span class="sxs-lookup"><span data-stu-id="d0f49-109">The values returned in the [**Record Object**](record-object.md) correspond to the four fields of the [**MSIFILEHASHINFO**](/windows/desktop/api/Msi/ns-msi-msifilehashinfo) structure returned by [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha).</span></span> <span data-ttu-id="d0f49-110">Нумерация четырех полей составляет 1 на основе [таблицы мсифилехаш](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="d0f49-110">The numbering of four fields is 1-based in the [MsiFileHash Table](msifilehash-table.md).</span></span>

-   <span data-ttu-id="d0f49-111">Поле 1 соответствует столбцу HashPart1.</span><span class="sxs-lookup"><span data-stu-id="d0f49-111">Field 1 corresponds to the HashPart1 column.</span></span>
-   <span data-ttu-id="d0f49-112">Поле 2 соответствует столбцу HashPart2.</span><span class="sxs-lookup"><span data-stu-id="d0f49-112">Field 2 corresponds to the HashPart2 column.</span></span>
-   <span data-ttu-id="d0f49-113">Поле 3 соответствует столбцу HashPart3.</span><span class="sxs-lookup"><span data-stu-id="d0f49-113">Field 3 corresponds to the HashPart3 column.</span></span>
-   <span data-ttu-id="d0f49-114">Поле 4 соответствует столбцу HashPart4.</span><span class="sxs-lookup"><span data-stu-id="d0f49-114">Field 4 corresponds to the HashPart4 column.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f49-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0f49-115">Syntax</span></span>


```JScript
Installer.FileHash(
  FilePath,
  Options
)
```



## <a name="parameters"></a><span data-ttu-id="d0f49-116">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0f49-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0f49-117">*Равно*</span><span class="sxs-lookup"><span data-stu-id="d0f49-117">*FilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="d0f49-118">Путь к файлу, который необходимо хэшировать.</span><span class="sxs-lookup"><span data-stu-id="d0f49-118">Path to the file that is to be hashed.</span></span>

</dd> <dt>

<span data-ttu-id="d0f49-119">*Параметры*</span><span class="sxs-lookup"><span data-stu-id="d0f49-119">*Options*</span></span> 
</dt> <dd>

<span data-ttu-id="d0f49-120">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="d0f49-120">Reserved for future use.</span></span>

<span data-ttu-id="d0f49-121">Значение этого параметра должно быть равно 0 (нулю).</span><span class="sxs-lookup"><span data-stu-id="d0f49-121">The value of this parameter must be 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0f49-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0f49-122">Return value</span></span>

<span data-ttu-id="d0f49-123">В случае успешного выполнения этот метод возвращает [**объект Record**](record-object.md) , содержащий хэш файла.</span><span class="sxs-lookup"><span data-stu-id="d0f49-123">If successful, this method returns a [**Record Object**](record-object.md) that contains the hash of the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0f49-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d0f49-124">Requirements</span></span>



| <span data-ttu-id="d0f49-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d0f49-125">Requirement</span></span> | <span data-ttu-id="d0f49-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d0f49-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f49-127">Версия</span><span class="sxs-lookup"><span data-stu-id="d0f49-127">Version</span></span><br/> | <span data-ttu-id="d0f49-128">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d0f49-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d0f49-129">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d0f49-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d0f49-130">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="d0f49-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d0f49-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d0f49-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="d0f49-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0f49-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d0f49-133">IID</span><span class="sxs-lookup"><span data-stu-id="d0f49-133">IID</span></span><br/>     | <span data-ttu-id="d0f49-134">IID \_ иинсталлер определен как 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d0f49-134">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="d0f49-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d0f49-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f49-136">Управление версиями файлов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d0f49-136">Default File Versioning</span></span>](default-file-versioning.md)
</dt> <dt>

[<span data-ttu-id="d0f49-137">Управление размерами и версиями файлов</span><span class="sxs-lookup"><span data-stu-id="d0f49-137">Manage File Sizes and Versions</span></span>](manage-file-sizes-and-versions.md)
</dt> <dt>

[<span data-ttu-id="d0f49-138">Таблица Мсифилехаш</span><span class="sxs-lookup"><span data-stu-id="d0f49-138">MsiFileHash Table</span></span>](msifilehash-table.md)
</dt> <dt>

[<span data-ttu-id="d0f49-139">**мсижетфилехаш**</span><span class="sxs-lookup"><span data-stu-id="d0f49-139">**MsiGetFileHash**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> </dl>

 

 




