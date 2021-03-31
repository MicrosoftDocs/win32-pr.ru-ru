---
title: Класс Win32_RDMSManagementData
description: Синхронизирует данные публикации для служб удаленный рабочий стол Management Services (RDMS).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSManagementData службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSManagementData, описание
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071216"
---
# <a name="win32_rdmsmanagementdata-class"></a><span data-ttu-id="92b3a-105">\_Класс Win32 рдмсманажементдата</span><span class="sxs-lookup"><span data-stu-id="92b3a-105">Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="92b3a-106">Синхронизирует данные публикации для служб удаленный рабочий стол Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="92b3a-106">Synchronizes publishing data for Remote Desktop Management Services (RDMS).</span></span>

<span data-ttu-id="92b3a-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="92b3a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b3a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92b3a-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a><span data-ttu-id="92b3a-109">Члены</span><span class="sxs-lookup"><span data-stu-id="92b3a-109">Members</span></span>

<span data-ttu-id="92b3a-110">Класс **Win32 \_ рдмсманажементдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="92b3a-110">The **Win32\_RDMSManagementData** class has these types of members:</span></span>

-   [<span data-ttu-id="92b3a-111">Методы</span><span class="sxs-lookup"><span data-stu-id="92b3a-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="92b3a-112">Методы</span><span class="sxs-lookup"><span data-stu-id="92b3a-112">Methods</span></span>

<span data-ttu-id="92b3a-113">Класс **Win32 \_ рдмсманажементдата** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="92b3a-113">The **Win32\_RDMSManagementData** class has these methods.</span></span>



| <span data-ttu-id="92b3a-114">Метод</span><span class="sxs-lookup"><span data-stu-id="92b3a-114">Method</span></span>                                                                                        | <span data-ttu-id="92b3a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="92b3a-115">Description</span></span>                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="92b3a-116">**синчронизеаллпублишингдата**</span><span class="sxs-lookup"><span data-stu-id="92b3a-116">**SynchronizeAllPublishingData**</span></span>](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | <span data-ttu-id="92b3a-117">Синхронизирует все данные публикации для RDMS.</span><span class="sxs-lookup"><span data-stu-id="92b3a-117">Synchronizes all publishing data for RDMS.</span></span><br/>                  |
| [<span data-ttu-id="92b3a-118">**синчронизепублишингдата**</span><span class="sxs-lookup"><span data-stu-id="92b3a-118">**SynchronizePublishingData**</span></span>](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | <span data-ttu-id="92b3a-119">Синхронизирует указанный набор публикуемых данных для RDMS.</span><span class="sxs-lookup"><span data-stu-id="92b3a-119">Synchronizes the specified set of publishing data for RDMS.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="92b3a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="92b3a-120">Requirements</span></span>



| <span data-ttu-id="92b3a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="92b3a-121">Requirement</span></span> | <span data-ttu-id="92b3a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="92b3a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b3a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92b3a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="92b3a-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="92b3a-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="92b3a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92b3a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="92b3a-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="92b3a-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="92b3a-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="92b3a-127">Namespace</span></span><br/>                | <span data-ttu-id="92b3a-128">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="92b3a-128">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="92b3a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="92b3a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="92b3a-130"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="92b3a-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="92b3a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="92b3a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92b3a-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92b3a-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="92b3a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92b3a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b3a-134">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="92b3a-134">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





