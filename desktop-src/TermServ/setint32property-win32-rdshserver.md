---
title: Метод SetInt32Property класса Win32_RDSHServer
description: Обновляет значение целочисленного свойства \_ объекта Win32 рдшсервер.
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetInt32Property
- Службы удаленных рабочих столов метода SetInt32Property, класс Win32_RDSHServer
- Класс Win32_RDSHServer службы удаленных рабочих столов, метод SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802123"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="7c049-106">Метод SetInt32Property \_ класса Win32 рдшсервер</span><span class="sxs-lookup"><span data-stu-id="7c049-106">SetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="7c049-107">Обновляет значение целочисленного свойства объекта [**Win32 \_ рдшсервер**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="7c049-107">Updates an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c049-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c049-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="7c049-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c049-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c049-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c049-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c049-111">Ключ, определяющий обновляемое свойство.</span><span class="sxs-lookup"><span data-stu-id="7c049-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="7c049-112">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c049-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c049-113">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="7c049-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c049-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c049-114">Return value</span></span>

<span data-ttu-id="7c049-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="7c049-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c049-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7c049-116">Requirements</span></span>



| <span data-ttu-id="7c049-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7c049-117">Requirement</span></span> | <span data-ttu-id="7c049-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7c049-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c049-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c049-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7c049-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7c049-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7c049-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c049-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7c049-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c049-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7c049-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7c049-123">Namespace</span></span><br/>                | <span data-ttu-id="7c049-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="7c049-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7c049-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7c049-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c049-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c049-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c049-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7c049-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c049-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c049-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7c049-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c049-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c049-130">**\_Рдшсервер Win32**</span><span class="sxs-lookup"><span data-stu-id="7c049-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





