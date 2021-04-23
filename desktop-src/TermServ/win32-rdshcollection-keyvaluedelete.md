---
title: Метод Кэйвалуеделете класса Win32_RDSHCollection
description: Удаляет из коллекции указанный ключ (и связанное значение).
ms.assetid: 968d6744-7b4a-45e5-87fb-90c408dbc771
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Кэйвалуеделете
- Службы удаленных рабочих столов метода Кэйвалуеделете, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод Кэйвалуеделете
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueDelete
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1b4b29aea7890817c8d3cd8599f6effceb53c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988514"
---
# <a name="keyvaluedelete-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="e71cb-106">Метод Кэйвалуеделете \_ класса Win32 рдшколлектион</span><span class="sxs-lookup"><span data-stu-id="e71cb-106">KeyValueDelete method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="e71cb-107">Удаляет из коллекции указанный ключ (и связанное значение).</span><span class="sxs-lookup"><span data-stu-id="e71cb-107">Deletes the specified key (and associated value) from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e71cb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e71cb-108">Syntax</span></span>


```mof
uint32 KeyValueDelete(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="e71cb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e71cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e71cb-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e71cb-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e71cb-111">Удаляемый ключ.</span><span class="sxs-lookup"><span data-stu-id="e71cb-111">The key to delete.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e71cb-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e71cb-112">Requirements</span></span>



| <span data-ttu-id="e71cb-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e71cb-113">Requirement</span></span> | <span data-ttu-id="e71cb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e71cb-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e71cb-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e71cb-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e71cb-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e71cb-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e71cb-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e71cb-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e71cb-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e71cb-118">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="e71cb-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e71cb-119">Namespace</span></span><br/>                | <span data-ttu-id="e71cb-120">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="e71cb-120">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e71cb-121">MOF</span><span class="sxs-lookup"><span data-stu-id="e71cb-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e71cb-122"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e71cb-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e71cb-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e71cb-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e71cb-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e71cb-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e71cb-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e71cb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e71cb-126">**\_Рдшколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="e71cb-126">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





