---
title: Класс Win32_RDAllowListFileAssociation
description: Описывает сопоставление типа опубликованного файла с удаленным приложением RemoteApp.
ms.assetid: 80cc8f5e-a7f0-458c-b05b-7822306f839a
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDAllowListFileAssociation службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDAllowListFileAssociation, описание
topic_type:
- apiref
api_name:
- Win32_RDAllowListFileAssociation
- Win32_RDAllowListFileAssociation.ExtName
- Win32_RDAllowListFileAssociation.AppAlias
- Win32_RDAllowListFileAssociation.ProgIdHint
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acbc74b5b0dab228a5c625863b4fcd0574b5f96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490590"
---
# <a name="win32_rdallowlistfileassociation-class"></a><span data-ttu-id="7aa7b-105">\_Класс Win32 рдалловлистфилеассоЦиатион</span><span class="sxs-lookup"><span data-stu-id="7aa7b-105">Win32\_RDAllowListFileAssociation class</span></span>

<span data-ttu-id="7aa7b-106">Описывает сопоставление типа опубликованного файла с удаленным приложением RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-106">Describes a published file type association with a RemoteApp.</span></span>

<span data-ttu-id="7aa7b-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aa7b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7aa7b-108">Syntax</span></span>

``` syntax
class Win32_RDAllowListFileAssociation
{
  string ExtName;
  string AppAlias;
  string ProgIdHint;
};
```

## <a name="members"></a><span data-ttu-id="7aa7b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="7aa7b-109">Members</span></span>

<span data-ttu-id="7aa7b-110">Класс **Win32 \_ рдалловлистфилеассоЦиатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7aa7b-110">The **Win32\_RDAllowListFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="7aa7b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7aa7b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7aa7b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7aa7b-112">Properties</span></span>

<span data-ttu-id="7aa7b-113">Класс **Win32 \_ рдалловлистфилеассоЦиатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-113">The **Win32\_RDAllowListFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7aa7b-114">**аппалиас**</span><span class="sxs-lookup"><span data-stu-id="7aa7b-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa7b-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7aa7b-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa7b-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aa7b-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7aa7b-117">Псевдоним удаленного приложения RemoteApp, связанного с расширением.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-117">Alias of the RemoteApp associated with the extension.</span></span>

</dd> <dt>

<span data-ttu-id="7aa7b-118">**екстнаме**</span><span class="sxs-lookup"><span data-stu-id="7aa7b-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa7b-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7aa7b-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa7b-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aa7b-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7aa7b-121">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="7aa7b-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7aa7b-122">Имя расширения, например TXT.</span><span class="sxs-lookup"><span data-stu-id="7aa7b-122">Name of the extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="7aa7b-123">**прогидхинт**</span><span class="sxs-lookup"><span data-stu-id="7aa7b-123">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7aa7b-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7aa7b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7aa7b-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7aa7b-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7aa7b-126">Указание для справки по открытию документов с этой ассоциацией файлов</span><span class="sxs-lookup"><span data-stu-id="7aa7b-126">Hint to help open documents with this file association</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7aa7b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="7aa7b-127">Requirements</span></span>



| <span data-ttu-id="7aa7b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="7aa7b-128">Requirement</span></span> | <span data-ttu-id="7aa7b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="7aa7b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7aa7b-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7aa7b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7aa7b-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7aa7b-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7aa7b-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7aa7b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7aa7b-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7aa7b-133">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="7aa7b-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7aa7b-134">Namespace</span></span><br/>                | <span data-ttu-id="7aa7b-135">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="7aa7b-135">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7aa7b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7aa7b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7aa7b-137"><dt>Тсаллов. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7aa7b-137"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="7aa7b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7aa7b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7aa7b-139"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7aa7b-139"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





