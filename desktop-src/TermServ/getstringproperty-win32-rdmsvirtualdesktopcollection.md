---
title: Метод Жетстрингпроперти класса Win32_RDMSVirtualDesktopCollection
description: Извлекает строковое свойство из коллекции виртуальных рабочих столов.
ms.assetid: 4a122fc5-1635-4d74-a90d-2347c0714fc7
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетстрингпроперти
- Службы удаленных рабочих столов метода Жетстрингпроперти, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Жетстрингпроперти
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242d973d7ec8d320ed589933567b337a035f0e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672506"
---
# <a name="getstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="ad09b-106">Метод Жетстрингпроперти \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="ad09b-106">GetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="ad09b-107">Извлекает строковое свойство из коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="ad09b-107">Retrieves a string property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad09b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad09b-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="ad09b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad09b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad09b-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ad09b-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad09b-111">Ключ, определяющий извлекаемое свойство.</span><span class="sxs-lookup"><span data-stu-id="ad09b-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ad09b-112">*Значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ad09b-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad09b-113">Строка, принимающая извлеченное значение.</span><span class="sxs-lookup"><span data-stu-id="ad09b-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad09b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad09b-114">Return value</span></span>

<span data-ttu-id="ad09b-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="ad09b-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad09b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ad09b-116">Requirements</span></span>



| <span data-ttu-id="ad09b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ad09b-117">Requirement</span></span> | <span data-ttu-id="ad09b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ad09b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad09b-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad09b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ad09b-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ad09b-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ad09b-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad09b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ad09b-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ad09b-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ad09b-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ad09b-123">Namespace</span></span><br/>                | <span data-ttu-id="ad09b-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="ad09b-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ad09b-125">MOF</span><span class="sxs-lookup"><span data-stu-id="ad09b-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad09b-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad09b-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad09b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ad09b-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad09b-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad09b-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ad09b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad09b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad09b-130">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="ad09b-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





