---
title: Метод Сетстрингпроперти класса Win32_RDMSVirtualDesktopCollection (Цертенролл. h)
description: Обновляет строковое свойство коллекции виртуальных рабочих столов.
ms.assetid: d76d5f77-3b51-41b9-8ec5-a737ddc0a9d3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетстрингпроперти
- Службы удаленных рабочих столов метода Сетстрингпроперти, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Сетстрингпроперти
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fd85ef6611cd02dc80ca66816c5c4ce13f6cd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672746"
---
# <a name="setstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="3c510-106">Метод Сетстрингпроперти \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="3c510-106">SetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="3c510-107">Обновляет строковое свойство коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="3c510-107">Updates a string property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c510-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c510-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="3c510-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c510-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c510-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c510-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c510-111">Ключ, определяющий обновляемое свойство.</span><span class="sxs-lookup"><span data-stu-id="3c510-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="3c510-112">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c510-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c510-113">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="3c510-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c510-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c510-114">Return value</span></span>

<span data-ttu-id="3c510-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="3c510-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c510-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3c510-116">Requirements</span></span>



| <span data-ttu-id="3c510-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3c510-117">Requirement</span></span> | <span data-ttu-id="3c510-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3c510-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c510-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c510-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c510-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3c510-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3c510-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c510-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c510-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3c510-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="3c510-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3c510-123">Namespace</span></span><br/>                | <span data-ttu-id="3c510-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="3c510-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3c510-125">Header</span><span class="sxs-lookup"><span data-stu-id="3c510-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c510-126"><dt>Цертенролл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c510-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="3c510-127">MOF</span><span class="sxs-lookup"><span data-stu-id="3c510-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c510-128"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c510-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c510-129">DLL</span><span class="sxs-lookup"><span data-stu-id="3c510-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c510-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c510-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3c510-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c510-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c510-132">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="3c510-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





