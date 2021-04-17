---
title: Метод SetInt32Property класса Win32_RDSHCollection
description: Обновляет значение целочисленного свойства \_ объекта Win32 рдшколлектион.
ms.assetid: 2a9a5d83-d147-43b3-b57c-6c744da0923d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetInt32Property
- Службы удаленных рабочих столов метода SetInt32Property, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 136bb8ccf34004f747829fb43ee8080ccd1d3132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682070"
---
# <a name="setint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="20e71-106">Метод SetInt32Property \_ класса Win32 рдшколлектион</span><span class="sxs-lookup"><span data-stu-id="20e71-106">SetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="20e71-107">Обновляет значение целочисленного свойства объекта [**Win32 \_ рдшколлектион**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="20e71-107">Updates an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="20e71-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20e71-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="20e71-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="20e71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20e71-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20e71-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20e71-111">Ключ, определяющий обновляемое свойство.</span><span class="sxs-lookup"><span data-stu-id="20e71-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="20e71-112">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="20e71-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20e71-113">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="20e71-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20e71-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20e71-114">Return value</span></span>

<span data-ttu-id="20e71-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="20e71-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="20e71-116">Требования</span><span class="sxs-lookup"><span data-stu-id="20e71-116">Requirements</span></span>



| <span data-ttu-id="20e71-117">Требование</span><span class="sxs-lookup"><span data-stu-id="20e71-117">Requirement</span></span> | <span data-ttu-id="20e71-118">Значение</span><span class="sxs-lookup"><span data-stu-id="20e71-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="20e71-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20e71-119">Minimum supported client</span></span><br/> | <span data-ttu-id="20e71-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="20e71-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="20e71-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20e71-121">Minimum supported server</span></span><br/> | <span data-ttu-id="20e71-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="20e71-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="20e71-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="20e71-123">Namespace</span></span><br/>                | <span data-ttu-id="20e71-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="20e71-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="20e71-125">MOF</span><span class="sxs-lookup"><span data-stu-id="20e71-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20e71-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20e71-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="20e71-127">DLL</span><span class="sxs-lookup"><span data-stu-id="20e71-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20e71-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20e71-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="20e71-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20e71-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20e71-130">**\_Рдшколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="20e71-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





