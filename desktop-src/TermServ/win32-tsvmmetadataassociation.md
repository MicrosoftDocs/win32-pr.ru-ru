---
title: Класс Win32_TSVmMetadataAssociation
description: Представляет связь между удаленный рабочий стол виртуальной машиной и ее свойствами метаданных.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSVmMetadataAssociation службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSVmMetadataAssociation, описание
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672480"
---
# <a name="win32_tsvmmetadataassociation-class"></a><span data-ttu-id="cf9c9-105">\_Класс Win32 тсвмметадатаассоЦиатион</span><span class="sxs-lookup"><span data-stu-id="cf9c9-105">Win32\_TSVmMetadataAssociation class</span></span>

<span data-ttu-id="cf9c9-106">Представляет связь между удаленный рабочий стол виртуальной машиной и ее свойствами метаданных.</span><span class="sxs-lookup"><span data-stu-id="cf9c9-106">Represents an association between a Remote Desktop virtual machine and its metadata properties.</span></span>

<span data-ttu-id="cf9c9-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="cf9c9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf9c9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf9c9-108">Syntax</span></span>

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a><span data-ttu-id="cf9c9-109">Члены</span><span class="sxs-lookup"><span data-stu-id="cf9c9-109">Members</span></span>

<span data-ttu-id="cf9c9-110">Класс **Win32 \_ тсвмметадатаассоЦиатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cf9c9-110">The **Win32\_TSVmMetadataAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="cf9c9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="cf9c9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf9c9-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="cf9c9-112">Properties</span></span>

<span data-ttu-id="cf9c9-113">Класс **Win32 \_ тсвмметадатаассоЦиатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cf9c9-113">The **Win32\_TSVmMetadataAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf9c9-114">**метадатаитем**</span><span class="sxs-lookup"><span data-stu-id="cf9c9-114">**MetadataItem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf9c9-115">Тип данных: **[ **Win32 \_ тсвмметадатаитем**](win32-tsvmmetadataitem.md)**</span><span class="sxs-lookup"><span data-stu-id="cf9c9-115">Data type: **[**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cf9c9-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf9c9-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf9c9-117">Экземпляр класса [**Win32 \_ тсвмметадатаитем**](win32-tsvmmetadataitem.md) , который представляет метаданные для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cf9c9-117">An instance of the [**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md) class that represents the metadata for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="cf9c9-118">**тсвм**</span><span class="sxs-lookup"><span data-stu-id="cf9c9-118">**TSVm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf9c9-119">Тип данных: **[ **Win32 \_ тсвм**](win32-tsvm.md)**</span><span class="sxs-lookup"><span data-stu-id="cf9c9-119">Data type: **[**Win32\_TSVm**](win32-tsvm.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cf9c9-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cf9c9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf9c9-121">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cf9c9-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cf9c9-122">Экземпляр класса [**Win32 \_ тсвм**](win32-tsvm.md) , представляющий виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="cf9c9-122">An instance of the [**Win32\_TSVm**](win32-tsvm.md) class that represents the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf9c9-123">Требования</span><span class="sxs-lookup"><span data-stu-id="cf9c9-123">Requirements</span></span>



| <span data-ttu-id="cf9c9-124">Требование</span><span class="sxs-lookup"><span data-stu-id="cf9c9-124">Requirement</span></span> | <span data-ttu-id="cf9c9-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cf9c9-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf9c9-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cf9c9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cf9c9-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cf9c9-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="cf9c9-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cf9c9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cf9c9-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf9c9-129">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="cf9c9-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cf9c9-130">Namespace</span></span><br/>                | <span data-ttu-id="cf9c9-131">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="cf9c9-131">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="cf9c9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="cf9c9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf9c9-133"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf9c9-133"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="cf9c9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="cf9c9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf9c9-135"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf9c9-135"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

