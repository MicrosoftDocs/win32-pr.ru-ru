---
title: Метод Жетстрингпроперти класса Win32_RDSHCollection
description: Извлекает значение свойства строки \_ объекта Win32 рдшколлектион.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетстрингпроперти
- Службы удаленных рабочих столов метода Жетстрингпроперти, класс Win32_RDSHCollection
- Класс Win32_RDSHCollection службы удаленных рабочих столов, метод Жетстрингпроперти
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1895f05317850374a4f4b24d407a4c4ace9c5db7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988344"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="294d8-106">Метод Жетстрингпроперти \_ класса Win32 рдшколлектион</span><span class="sxs-lookup"><span data-stu-id="294d8-106">GetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="294d8-107">Извлекает значение свойства строки объекта [**Win32 \_ рдшколлектион**](win32-rdshcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="294d8-107">Retrieves a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="294d8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="294d8-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="294d8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="294d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="294d8-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="294d8-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="294d8-111">Ключ, определяющий извлекаемое свойство.</span><span class="sxs-lookup"><span data-stu-id="294d8-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="294d8-112">*Значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="294d8-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="294d8-113">Получает полученное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="294d8-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="294d8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="294d8-114">Return value</span></span>

<span data-ttu-id="294d8-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="294d8-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="294d8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="294d8-116">Requirements</span></span>



| <span data-ttu-id="294d8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="294d8-117">Requirement</span></span> | <span data-ttu-id="294d8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="294d8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="294d8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="294d8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="294d8-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="294d8-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="294d8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="294d8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="294d8-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="294d8-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="294d8-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="294d8-123">Namespace</span></span><br/>                | <span data-ttu-id="294d8-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="294d8-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="294d8-125">MOF</span><span class="sxs-lookup"><span data-stu-id="294d8-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="294d8-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="294d8-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="294d8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="294d8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="294d8-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="294d8-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="294d8-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="294d8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="294d8-130">**\_Рдшколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="294d8-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





