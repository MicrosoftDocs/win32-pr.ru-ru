---
title: Метод Жетстрингпроперти класса Win32_RDSHServer
description: Извлекает значение свойства строки \_ объекта Win32 рдшсервер.
ms.assetid: 136cd213-86a6-472a-8853-8d05f992309a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетстрингпроперти
- Службы удаленных рабочих столов метода Жетстрингпроперти, класс Win32_RDSHServer
- Класс Win32_RDSHServer службы удаленных рабочих столов, метод Жетстрингпроперти
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619a034e0a2f89270d21bf0c4fc297b4248cef59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493008"
---
# <a name="getstringproperty-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="e31a1-106">Метод Жетстрингпроперти \_ класса Win32 рдшсервер</span><span class="sxs-lookup"><span data-stu-id="e31a1-106">GetStringProperty method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="e31a1-107">Извлекает значение свойства строки объекта [**Win32 \_ рдшсервер**](win32-rdshserver.md) .</span><span class="sxs-lookup"><span data-stu-id="e31a1-107">Retrieves a string property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31a1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e31a1-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="e31a1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e31a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31a1-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e31a1-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31a1-111">Ключ, определяющий извлекаемое свойство.</span><span class="sxs-lookup"><span data-stu-id="e31a1-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e31a1-112">*Значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e31a1-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e31a1-113">Получает полученное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="e31a1-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e31a1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e31a1-114">Return value</span></span>

<span data-ttu-id="e31a1-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="e31a1-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e31a1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e31a1-116">Requirements</span></span>



| <span data-ttu-id="e31a1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e31a1-117">Requirement</span></span> | <span data-ttu-id="e31a1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e31a1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e31a1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e31a1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e31a1-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e31a1-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e31a1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e31a1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e31a1-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e31a1-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e31a1-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e31a1-123">Namespace</span></span><br/>                | <span data-ttu-id="e31a1-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="e31a1-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e31a1-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e31a1-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e31a1-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e31a1-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e31a1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e31a1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e31a1-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e31a1-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e31a1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e31a1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31a1-130">**\_Рдшсервер Win32**</span><span class="sxs-lookup"><span data-stu-id="e31a1-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





