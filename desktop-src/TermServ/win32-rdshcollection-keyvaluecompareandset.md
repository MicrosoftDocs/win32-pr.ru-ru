---
title: Метод Кэйвалуекомпареандсет класса Win32_RDSHCollection
description: Сравнивает указанный ключ в коллекции с сравниваемый операнд; Если они совпадают, для ключа задается новое значение. Если ключ не существует, метод вставит ключ в коллекцию.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Кэйвалуекомпареандсет
- Службы удаленных рабочих столов метода Кэйвалуекомпареандсет, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод Кэйвалуекомпареандсет
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891746"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="9b890-107">Метод Кэйвалуекомпареандсет \_ класса Win32 рдшколлектион</span><span class="sxs-lookup"><span data-stu-id="9b890-107">KeyValueCompareAndSet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="9b890-108">Сравнивает указанный ключ в коллекции с сравниваемый операнд; Если они совпадают, для ключа задается новое значение.</span><span class="sxs-lookup"><span data-stu-id="9b890-108">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="9b890-109">Если ключ не существует, метод вставит ключ в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="9b890-109">If the key does not exist, the method will insert the key into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b890-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b890-110">Syntax</span></span>


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a><span data-ttu-id="9b890-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b890-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b890-112">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b890-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b890-113">Сравниваемый ключ.</span><span class="sxs-lookup"><span data-stu-id="9b890-113">The key to compare.</span></span>

</dd> <dt>

<span data-ttu-id="9b890-114">*NewValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b890-114">*NewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b890-115">Новое значение.</span><span class="sxs-lookup"><span data-stu-id="9b890-115">The new value.</span></span>

</dd> <dt>

<span data-ttu-id="9b890-116">*Сравниваемый операнд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b890-116">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b890-117">Строка для сравнения ключа.</span><span class="sxs-lookup"><span data-stu-id="9b890-117">The string to compare the key to.</span></span>

</dd> <dt>

<span data-ttu-id="9b890-118">*Инитиалвалуе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9b890-118">*InitialValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b890-119">При успешном или неудачном завершении содержит начальное значение ключа.</span><span class="sxs-lookup"><span data-stu-id="9b890-119">On success or failure, contains the initial value of the key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b890-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b890-120">Remarks</span></span>

<span data-ttu-id="9b890-121">Обратите внимание, что этот метод может извлекать значение ключа и, как таковой, инкапсулирует функциональность [**кэйвалуежет**](win32-rdshcollection-keyvalueget.md).</span><span class="sxs-lookup"><span data-stu-id="9b890-121">Note that this method can retrieve the value of the key, and as such encapsulates the functionality of [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b890-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9b890-122">Requirements</span></span>



| <span data-ttu-id="9b890-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9b890-123">Requirement</span></span> | <span data-ttu-id="9b890-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9b890-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b890-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b890-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9b890-126">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9b890-126">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9b890-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b890-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9b890-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9b890-128">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="9b890-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9b890-129">Namespace</span></span><br/>                | <span data-ttu-id="9b890-130">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="9b890-130">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9b890-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9b890-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b890-132"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b890-132"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b890-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9b890-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b890-134"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b890-134"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9b890-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b890-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b890-136">**\_Рдшколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="9b890-136">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





