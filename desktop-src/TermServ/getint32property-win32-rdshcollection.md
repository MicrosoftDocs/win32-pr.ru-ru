---
title: Метод GetInt32Property класса Win32_RDSHCollection (Microsoft. Diagnostics. аппаналисис. h)
description: Извлекает значение целочисленного свойства \_ объекта Рдшколлектион Win32.
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода GetInt32Property
- Службы удаленных рабочих столов метода GetInt32Property, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5cc29234fe3bb1b92e68e728423931da965391f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801456"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="7da6e-106">Метод GetInt32Property \_ класса Win32 рдшколлектион</span><span class="sxs-lookup"><span data-stu-id="7da6e-106">GetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="7da6e-107">Извлекает значение целочисленного свойства объекта [**\_ рдшколлектион Win32**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="7da6e-107">Retrieves an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7da6e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7da6e-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="7da6e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7da6e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7da6e-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7da6e-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7da6e-111">Ключ, определяющий извлекаемое свойство.</span><span class="sxs-lookup"><span data-stu-id="7da6e-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="7da6e-112">*Значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7da6e-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7da6e-113">Получает полученное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="7da6e-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7da6e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7da6e-114">Return value</span></span>

<span data-ttu-id="7da6e-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="7da6e-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7da6e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7da6e-116">Requirements</span></span>



| <span data-ttu-id="7da6e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7da6e-117">Requirement</span></span> | <span data-ttu-id="7da6e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7da6e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7da6e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7da6e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7da6e-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7da6e-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="7da6e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7da6e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7da6e-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7da6e-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="7da6e-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7da6e-123">Namespace</span></span><br/>                | <span data-ttu-id="7da6e-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="7da6e-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="7da6e-125">Header</span><span class="sxs-lookup"><span data-stu-id="7da6e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7da6e-126"><dt>Microsoft. Diagnostics. аппаналисис. h</dt></span><span class="sxs-lookup"><span data-stu-id="7da6e-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="7da6e-127">MOF</span><span class="sxs-lookup"><span data-stu-id="7da6e-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7da6e-128"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7da6e-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="7da6e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7da6e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7da6e-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7da6e-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="7da6e-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7da6e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7da6e-132">**\_Рдшколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="7da6e-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





