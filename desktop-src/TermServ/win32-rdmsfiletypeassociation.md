---
title: Класс Win32_RDMSFileTypeAssociation
description: Управляет сопоставлением типов файлов для опубликованного приложения.
ms.assetid: 22c945cb-4c47-431a-bc9b-d33ba15c8ab3
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSFileTypeAssociation службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSFileTypeAssociation, описание
topic_type:
- apiref
api_name:
- Win32_RDMSFileTypeAssociation
- Win32_RDMSFileTypeAssociation.AppAlias
- Win32_RDMSFileTypeAssociation.PoolName
- Win32_RDMSFileTypeAssociation.ExtName
- Win32_RDMSFileTypeAssociation.ProgIdHint
- Win32_RDMSFileTypeAssociation.IconPath
- Win32_RDMSFileTypeAssociation.IconIndex
- Win32_RDMSFileTypeAssociation.IconContents
- Win32_RDMSFileTypeAssociation.IsPrimaryHandler
- Win32_RDMSFileTypeAssociation.IsPublished
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2e569077bf47a2b0eba63db39ae1e86c39feb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414840"
---
# <a name="win32_rdmsfiletypeassociation-class"></a><span data-ttu-id="c4672-105">\_Класс Win32 рдмсфилетипеассоЦиатион</span><span class="sxs-lookup"><span data-stu-id="c4672-105">Win32\_RDMSFileTypeAssociation class</span></span>

<span data-ttu-id="c4672-106">Управляет сопоставлением типов файлов для опубликованного приложения.</span><span class="sxs-lookup"><span data-stu-id="c4672-106">Manages a file type association for a published application.</span></span>

<span data-ttu-id="c4672-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c4672-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4672-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4672-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSFileTypeAssociation
{
  string  AppAlias;
  string  PoolName;
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean IsPrimaryHandler;
  boolean IsPublished;
};
```

## <a name="members"></a><span data-ttu-id="c4672-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c4672-109">Members</span></span>

<span data-ttu-id="c4672-110">Класс **Win32 \_ рдмсфилетипеассоЦиатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c4672-110">The **Win32\_RDMSFileTypeAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="c4672-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4672-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4672-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c4672-112">Properties</span></span>

<span data-ttu-id="c4672-113">Класс **Win32 \_ рдмсфилетипеассоЦиатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c4672-113">The **Win32\_RDMSFileTypeAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4672-114">**аппалиас**</span><span class="sxs-lookup"><span data-stu-id="c4672-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4672-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4672-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4672-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4672-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4672-117">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4672-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c4672-118">Возвращает и задает псевдоним приложения, связанного с типом файла.</span><span class="sxs-lookup"><span data-stu-id="c4672-118">Gets and sets the alias of the application that is associated with the file type.</span></span>

</dd> <dt>

<span data-ttu-id="c4672-119">**екстнаме**</span><span class="sxs-lookup"><span data-stu-id="c4672-119">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4672-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4672-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4672-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4672-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4672-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4672-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c4672-123">Возвращает имя расширения файла.</span><span class="sxs-lookup"><span data-stu-id="c4672-123">Gets the name of the file extension.</span></span>

</dd> <dt>

<span data-ttu-id="c4672-124">**иконконтентс**</span><span class="sxs-lookup"><span data-stu-id="c4672-124">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4672-125">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c4672-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c4672-126">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4672-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4672-127">Возвращает и задает содержимое значка для типа файла.</span><span class="sxs-lookup"><span data-stu-id="c4672-127">Gets and sets the content of the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="c4672-128">**икониндекс**</span><span class="sxs-lookup"><span data-stu-id="c4672-128">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4672-129">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c4672-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c4672-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4672-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4672-131">Возвращает и задает индекс значка для типа файла.</span><span class="sxs-lookup"><span data-stu-id="c4672-131">Gets and sets the index to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="c4672-132">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="c4672-132">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4672-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4672-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4672-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4672-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4672-135">Возвращает и задает путь к значку для типа файла.</span><span class="sxs-lookup"><span data-stu-id="c4672-135">Gets and sets the path to the icon for the file type.</span></span>

</dd> <dt>

<span data-ttu-id="c4672-136">**испримарихандлер**</span><span class="sxs-lookup"><span data-stu-id="c4672-136">**IsPrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4672-137">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c4672-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4672-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4672-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4672-139">Возвращает и задает значение, указывающее, относится ли сопоставление типа файла к основному обработчику.</span><span class="sxs-lookup"><span data-stu-id="c4672-139">Gets and sets a value that indicates whether the file type association is for the primary handler.</span></span> <span data-ttu-id="c4672-140">**Значение true** , если тип файла связан с основным обработчиком; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c4672-140">**TRUE** if the file type association is for the primary handler; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c4672-141">**IsPublished**</span><span class="sxs-lookup"><span data-stu-id="c4672-141">**IsPublished**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4672-142">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="c4672-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c4672-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4672-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c4672-144">Публикуется ли этот ФТА.</span><span class="sxs-lookup"><span data-stu-id="c4672-144">Whether this FTA is published.</span></span>

<span data-ttu-id="c4672-145">Возвращает и задает значение, указывающее, опубликована ли ассоциация типа файла.</span><span class="sxs-lookup"><span data-stu-id="c4672-145">Gets and sets a value that indicates whether the file type association is published.</span></span> <span data-ttu-id="c4672-146">**Значение true** , если сопоставление типа файла Опубликовано; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="c4672-146">**TRUE** if the file type association is published; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="c4672-147">**PoolName**</span><span class="sxs-lookup"><span data-stu-id="c4672-147">**PoolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4672-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4672-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4672-149">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c4672-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c4672-150">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c4672-150">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c4672-151">Возвращает и задает имя пула приложений для сопоставления типа файла.</span><span class="sxs-lookup"><span data-stu-id="c4672-151">Gets and sets the name of the application pool for the file type association.</span></span>

</dd> <dt>

<span data-ttu-id="c4672-152">**прогидхинт**</span><span class="sxs-lookup"><span data-stu-id="c4672-152">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4672-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c4672-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4672-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c4672-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4672-155">Возвращает указание, помогающее пользователям открыть расширение файла.</span><span class="sxs-lookup"><span data-stu-id="c4672-155">Gets a hint to help users open the file extension.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4672-156">Требования</span><span class="sxs-lookup"><span data-stu-id="c4672-156">Requirements</span></span>



| <span data-ttu-id="c4672-157">Требование</span><span class="sxs-lookup"><span data-stu-id="c4672-157">Requirement</span></span> | <span data-ttu-id="c4672-158">Значение</span><span class="sxs-lookup"><span data-stu-id="c4672-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4672-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c4672-159">Minimum supported client</span></span><br/> | <span data-ttu-id="c4672-160">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c4672-160">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c4672-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c4672-161">Minimum supported server</span></span><br/> | <span data-ttu-id="c4672-162">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c4672-162">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c4672-163">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c4672-163">Namespace</span></span><br/>                | <span data-ttu-id="c4672-164">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="c4672-164">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c4672-165">MOF</span><span class="sxs-lookup"><span data-stu-id="c4672-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4672-166"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4672-166"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4672-167">DLL</span><span class="sxs-lookup"><span data-stu-id="c4672-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4672-168"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4672-168"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c4672-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c4672-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4672-170">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="c4672-170">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

