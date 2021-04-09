---
title: Метод Кэйвалуежет класса Win32_RDSHCollection
description: Извлекает значение, связанное с указанным ключом в коллекции.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Кэйвалуежет
- Службы удаленных рабочих столов метода Кэйвалуежет, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод Кэйвалуежет
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5304cca379106094d4d00b9a0b5506c8df7075a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891745"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="1bcbc-106">Метод Кэйвалуежет \_ класса Win32 рдшколлектион</span><span class="sxs-lookup"><span data-stu-id="1bcbc-106">KeyValueGet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="1bcbc-107">Извлекает значение, связанное с указанным ключом в коллекции.</span><span class="sxs-lookup"><span data-stu-id="1bcbc-107">Retrieves the value associated with the specified key in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bcbc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bcbc-108">Syntax</span></span>


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="1bcbc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bcbc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bcbc-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1bcbc-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1bcbc-111">Ключ, определяющий значение, которое вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="1bcbc-111">The key that identifies the value you wish to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="1bcbc-112">*Значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1bcbc-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1bcbc-113">При успешном выполнении возвращает значение, связанное с указанным ключом.</span><span class="sxs-lookup"><span data-stu-id="1bcbc-113">On success, returns the value associated with the specified key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bcbc-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1bcbc-114">Requirements</span></span>



| <span data-ttu-id="1bcbc-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1bcbc-115">Requirement</span></span> | <span data-ttu-id="1bcbc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1bcbc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bcbc-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1bcbc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1bcbc-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1bcbc-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1bcbc-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1bcbc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1bcbc-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1bcbc-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="1bcbc-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1bcbc-121">Namespace</span></span><br/>                | <span data-ttu-id="1bcbc-122">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="1bcbc-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1bcbc-123">MOF</span><span class="sxs-lookup"><span data-stu-id="1bcbc-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bcbc-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bcbc-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bcbc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1bcbc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bcbc-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bcbc-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1bcbc-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bcbc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bcbc-128">**\_Рдшколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="1bcbc-128">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





