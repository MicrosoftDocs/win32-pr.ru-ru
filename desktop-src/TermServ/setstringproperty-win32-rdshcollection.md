---
title: Метод Сетстрингпроперти класса Win32_RDSHCollection (Цертенролл. h)
description: Обновляет значение свойства строки \_ объекта Win32 рдшколлектион.
ms.assetid: 6981b47a-5480-44f5-90e3-f64d439fa2aa
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетстрингпроперти
- Службы удаленных рабочих столов метода Сетстрингпроперти, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод Сетстрингпроперти
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2606c195822432138ee67576db54f945c6834cfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672745"
---
# <a name="setstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="eee18-106">Метод Сетстрингпроперти \_ класса Win32 рдшколлектион</span><span class="sxs-lookup"><span data-stu-id="eee18-106">SetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="eee18-107">Обновляет значение свойства строки объекта [**Win32 \_ рдшколлектион**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="eee18-107">Updates a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="eee18-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eee18-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="eee18-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="eee18-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eee18-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eee18-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eee18-111">Ключ, определяющий обновляемое свойство.</span><span class="sxs-lookup"><span data-stu-id="eee18-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="eee18-112">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="eee18-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eee18-113">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="eee18-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eee18-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="eee18-114">Return value</span></span>

<span data-ttu-id="eee18-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="eee18-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="eee18-116">Требования</span><span class="sxs-lookup"><span data-stu-id="eee18-116">Requirements</span></span>



| <span data-ttu-id="eee18-117">Требование</span><span class="sxs-lookup"><span data-stu-id="eee18-117">Requirement</span></span> | <span data-ttu-id="eee18-118">Значение</span><span class="sxs-lookup"><span data-stu-id="eee18-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eee18-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eee18-119">Minimum supported client</span></span><br/> | <span data-ttu-id="eee18-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="eee18-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="eee18-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eee18-121">Minimum supported server</span></span><br/> | <span data-ttu-id="eee18-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eee18-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="eee18-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eee18-123">Namespace</span></span><br/>                | <span data-ttu-id="eee18-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="eee18-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="eee18-125">Header</span><span class="sxs-lookup"><span data-stu-id="eee18-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="eee18-126"><dt>Цертенролл. h</dt></span><span class="sxs-lookup"><span data-stu-id="eee18-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="eee18-127">MOF</span><span class="sxs-lookup"><span data-stu-id="eee18-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eee18-128"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eee18-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="eee18-129">DLL</span><span class="sxs-lookup"><span data-stu-id="eee18-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eee18-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eee18-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="eee18-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eee18-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee18-132">**\_Рдшколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="eee18-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





