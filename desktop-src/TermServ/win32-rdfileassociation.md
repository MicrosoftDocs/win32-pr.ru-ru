---
title: Класс Win32_RDFileAssociation
description: Представляет сопоставление типов файлов для RemoteApp.
ms.assetid: 9ecf6fa5-36f0-4b37-9d59-781b41c1d90c
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDFileAssociation службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDFileAssociation, описание
topic_type:
- apiref
api_name:
- Win32_RDFileAssociation
- Win32_RDFileAssociation.ExtName
- Win32_RDFileAssociation.ProgIdHint
- Win32_RDFileAssociation.IconPath
- Win32_RDFileAssociation.IconIndex
- Win32_RDFileAssociation.IconContents
- Win32_RDFileAssociation.PrimaryHandler
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac64cd38bdad748c64fe6f52cb7a6da8d8220cba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988518"
---
# <a name="win32_rdfileassociation-class"></a><span data-ttu-id="174f9-105">\_Класс Win32 рдфилеассоЦиатион</span><span class="sxs-lookup"><span data-stu-id="174f9-105">Win32\_RDFileAssociation class</span></span>

<span data-ttu-id="174f9-106">Представляет сопоставление типов файлов для RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="174f9-106">Represents a file type association for a RemoteApp.</span></span>

<span data-ttu-id="174f9-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="174f9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="174f9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="174f9-108">Syntax</span></span>

``` syntax
class Win32_RDFileAssociation
{
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="174f9-109">Члены</span><span class="sxs-lookup"><span data-stu-id="174f9-109">Members</span></span>

<span data-ttu-id="174f9-110">Класс **Win32 \_ рдфилеассоЦиатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="174f9-110">The **Win32\_RDFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="174f9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="174f9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="174f9-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="174f9-112">Properties</span></span>

<span data-ttu-id="174f9-113">Класс **Win32 \_ рдфилеассоЦиатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="174f9-113">The **Win32\_RDFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="174f9-114">**екстнаме**</span><span class="sxs-lookup"><span data-stu-id="174f9-114">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="174f9-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="174f9-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="174f9-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="174f9-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="174f9-117">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="174f9-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="174f9-118">Имя расширения имени файла, например TXT.</span><span class="sxs-lookup"><span data-stu-id="174f9-118">The name of the file name extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="174f9-119">**иконконтентс**</span><span class="sxs-lookup"><span data-stu-id="174f9-119">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="174f9-120">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="174f9-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="174f9-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="174f9-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="174f9-122">Содержимое значка для этого сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="174f9-122">The contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="174f9-123">**икониндекс**</span><span class="sxs-lookup"><span data-stu-id="174f9-123">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="174f9-124">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="174f9-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="174f9-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="174f9-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="174f9-126">Индекс значка в файле.</span><span class="sxs-lookup"><span data-stu-id="174f9-126">The index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="174f9-127">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="174f9-127">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="174f9-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="174f9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="174f9-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="174f9-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="174f9-130">Путь к файлу значка для этого сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="174f9-130">The file path to the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="174f9-131">**примарихандлер**</span><span class="sxs-lookup"><span data-stu-id="174f9-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="174f9-132">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="174f9-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="174f9-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="174f9-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="174f9-134">Указывает, относится ли эта ассоциация к основному обработчику.</span><span class="sxs-lookup"><span data-stu-id="174f9-134">Indicates whether this association is for a primary handler.</span></span>

</dd> <dt>

<span data-ttu-id="174f9-135">**прогидхинт**</span><span class="sxs-lookup"><span data-stu-id="174f9-135">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="174f9-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="174f9-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="174f9-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="174f9-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="174f9-138">Указание, помогающее открывать документы с этой ассоциацией файлов.</span><span class="sxs-lookup"><span data-stu-id="174f9-138">The Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="174f9-139">Требования</span><span class="sxs-lookup"><span data-stu-id="174f9-139">Requirements</span></span>



| <span data-ttu-id="174f9-140">Требование</span><span class="sxs-lookup"><span data-stu-id="174f9-140">Requirement</span></span> | <span data-ttu-id="174f9-141">Значение</span><span class="sxs-lookup"><span data-stu-id="174f9-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="174f9-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="174f9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="174f9-143">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="174f9-143">None supported</span></span><br/>                                                               |
| <span data-ttu-id="174f9-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="174f9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="174f9-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="174f9-145">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="174f9-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="174f9-146">Namespace</span></span><br/>                | <span data-ttu-id="174f9-147">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="174f9-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="174f9-148">MOF</span><span class="sxs-lookup"><span data-stu-id="174f9-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="174f9-149"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="174f9-149"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="174f9-150">DLL</span><span class="sxs-lookup"><span data-stu-id="174f9-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="174f9-151"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="174f9-151"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





