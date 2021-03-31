---
title: Метод SetInt32Property класса Win32_RDMSVirtualDesktopCollection
description: Обновляет целочисленное свойство коллекции виртуальных рабочих столов.
ms.assetid: 2ea27385-5100-4e88-ad11-df5e439d0815
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetInt32Property
- Службы удаленных рабочих столов метода SetInt32Property, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c2a93a52ce79bc185cd37dd9ac93e5b420b5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137342"
---
# <a name="setint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="258cb-106">Метод SetInt32Property \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="258cb-106">SetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="258cb-107">Обновляет целочисленное свойство коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="258cb-107">Updates an integer property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="258cb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="258cb-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="258cb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="258cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="258cb-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="258cb-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="258cb-111">Ключ, определяющий обновляемое свойство.</span><span class="sxs-lookup"><span data-stu-id="258cb-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="258cb-112">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="258cb-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="258cb-113">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="258cb-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="258cb-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="258cb-114">Return value</span></span>

<span data-ttu-id="258cb-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="258cb-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="258cb-116">Требования</span><span class="sxs-lookup"><span data-stu-id="258cb-116">Requirements</span></span>



| <span data-ttu-id="258cb-117">Требование</span><span class="sxs-lookup"><span data-stu-id="258cb-117">Requirement</span></span> | <span data-ttu-id="258cb-118">Значение</span><span class="sxs-lookup"><span data-stu-id="258cb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="258cb-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="258cb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="258cb-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="258cb-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="258cb-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="258cb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="258cb-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="258cb-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="258cb-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="258cb-123">Namespace</span></span><br/>                | <span data-ttu-id="258cb-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="258cb-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="258cb-125">MOF</span><span class="sxs-lookup"><span data-stu-id="258cb-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="258cb-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="258cb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="258cb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="258cb-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="258cb-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="258cb-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="258cb-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="258cb-130">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="258cb-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





