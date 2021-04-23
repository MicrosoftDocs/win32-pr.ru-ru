---
title: Класс Win32_RDCentralPublishedFileAssociation
description: Сведения о расширении файла, связанном с приложением.
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDCentralPublishedFileAssociation службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDCentralPublishedFileAssociation, описание
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a0f1c9bf7905504ee3aa2ba6fff7e9804f4747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492741"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a><span data-ttu-id="30204-105">\_Класс Win32 рдцентралпублишедфилеассоЦиатион</span><span class="sxs-lookup"><span data-stu-id="30204-105">Win32\_RDCentralPublishedFileAssociation class</span></span>

<span data-ttu-id="30204-106">Сведения о расширении файла, связанном с приложением</span><span class="sxs-lookup"><span data-stu-id="30204-106">Info for a file extension associated with an application</span></span>

<span data-ttu-id="30204-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="30204-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="30204-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30204-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="30204-109">Члены</span><span class="sxs-lookup"><span data-stu-id="30204-109">Members</span></span>

<span data-ttu-id="30204-110">Класс **Win32 \_ рдцентралпублишедфилеассоЦиатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="30204-110">The **Win32\_RDCentralPublishedFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="30204-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="30204-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30204-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="30204-112">Properties</span></span>

<span data-ttu-id="30204-113">Класс **Win32 \_ рдцентралпублишедфилеассоЦиатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="30204-113">The **Win32\_RDCentralPublishedFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30204-114">**аппалиас**</span><span class="sxs-lookup"><span data-stu-id="30204-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30204-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="30204-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30204-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="30204-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30204-117">Псевдоним RemoteApp для сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="30204-117">Alias of the file association's RemoteApp.</span></span>

</dd> <dt>

<span data-ttu-id="30204-118">**екстнаме**</span><span class="sxs-lookup"><span data-stu-id="30204-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30204-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="30204-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30204-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="30204-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="30204-121">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="30204-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="30204-122">Имя расширения (например, txt).</span><span class="sxs-lookup"><span data-stu-id="30204-122">Name of the extension (e.g. .txt).</span></span>

</dd> <dt>

<span data-ttu-id="30204-123">**фармалиас**</span><span class="sxs-lookup"><span data-stu-id="30204-123">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30204-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="30204-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30204-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="30204-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30204-126">Псевдоним фермы Ремотеапп'с сопоставления файлов</span><span class="sxs-lookup"><span data-stu-id="30204-126">Alias of the file association's RemoteApp's Farm</span></span>

</dd> <dt>

<span data-ttu-id="30204-127">**иконконтентс**</span><span class="sxs-lookup"><span data-stu-id="30204-127">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30204-128">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="30204-128">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="30204-129">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="30204-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30204-130">Содержимое значка для этого сопоставления файлов.</span><span class="sxs-lookup"><span data-stu-id="30204-130">Contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="30204-131">**примарихандлер**</span><span class="sxs-lookup"><span data-stu-id="30204-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30204-132">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="30204-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="30204-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="30204-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30204-134">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="30204-134">Reserved for future use.</span></span> <span data-ttu-id="30204-135">Всегда будет иметь **значение true**.</span><span class="sxs-lookup"><span data-stu-id="30204-135">Will always be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="30204-136">**прогидхинт**</span><span class="sxs-lookup"><span data-stu-id="30204-136">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30204-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="30204-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="30204-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="30204-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="30204-139">Указание, помогающее открывать документы с этой ассоциацией файлов.</span><span class="sxs-lookup"><span data-stu-id="30204-139">Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="30204-140">Требования</span><span class="sxs-lookup"><span data-stu-id="30204-140">Requirements</span></span>



| <span data-ttu-id="30204-141">Требование</span><span class="sxs-lookup"><span data-stu-id="30204-141">Requirement</span></span> | <span data-ttu-id="30204-142">Значение</span><span class="sxs-lookup"><span data-stu-id="30204-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30204-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30204-143">Minimum supported client</span></span><br/> | <span data-ttu-id="30204-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="30204-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="30204-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30204-145">Minimum supported server</span></span><br/> | <span data-ttu-id="30204-146">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30204-146">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="30204-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="30204-147">Namespace</span></span><br/>                | <span data-ttu-id="30204-148">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="30204-148">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="30204-149">MOF</span><span class="sxs-lookup"><span data-stu-id="30204-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30204-150"><dt>Тскпуб. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30204-150"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="30204-151">DLL</span><span class="sxs-lookup"><span data-stu-id="30204-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30204-152"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30204-152"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

