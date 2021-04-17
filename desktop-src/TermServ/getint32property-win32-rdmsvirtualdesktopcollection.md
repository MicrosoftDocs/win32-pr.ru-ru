---
title: Метод GetInt32Property класса Win32_RDMSVirtualDesktopCollection (Microsoft. Diagnostics. аппаналисис. h)
description: Извлекает целочисленное свойство из коллекции виртуальных рабочих столов.
ms.assetid: 18ffca65-e7c0-4b17-902f-d74b2a81aba2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода GetInt32Property
- Службы удаленных рабочих столов метода GetInt32Property, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e8e5518590bece8e8b904ea56bf7572b436b66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672507"
---
# <a name="getint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="9d868-106">Метод GetInt32Property \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="9d868-106">GetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="9d868-107">Извлекает целочисленное свойство из коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="9d868-107">Retrieves an integer property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d868-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9d868-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="9d868-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d868-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d868-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9d868-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d868-111">Ключ, определяющий извлекаемое свойство.</span><span class="sxs-lookup"><span data-stu-id="9d868-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9d868-112">*Значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9d868-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d868-113">Целое число, получающее полученное значение.</span><span class="sxs-lookup"><span data-stu-id="9d868-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d868-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d868-114">Return value</span></span>

<span data-ttu-id="9d868-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="9d868-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d868-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9d868-116">Requirements</span></span>



| <span data-ttu-id="9d868-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9d868-117">Requirement</span></span> | <span data-ttu-id="9d868-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9d868-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d868-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d868-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9d868-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9d868-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="9d868-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d868-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9d868-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9d868-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="9d868-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9d868-123">Namespace</span></span><br/>                | <span data-ttu-id="9d868-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="9d868-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="9d868-125">Header</span><span class="sxs-lookup"><span data-stu-id="9d868-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d868-126"><dt>Microsoft. Diagnostics. аппаналисис. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d868-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="9d868-127">MOF</span><span class="sxs-lookup"><span data-stu-id="9d868-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d868-128"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d868-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="9d868-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9d868-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d868-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d868-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="9d868-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d868-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d868-132">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="9d868-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





