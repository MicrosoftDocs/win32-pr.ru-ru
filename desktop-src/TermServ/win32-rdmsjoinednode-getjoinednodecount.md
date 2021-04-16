---
title: Метод Жетжоинеднодекаунт класса Win32_RDMSJoinedNode
description: Возвращает число серверов, на которых установлены указанные роли.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетжоинеднодекаунт
- Службы удаленных рабочих столов метода Жетжоинеднодекаунт, класс Win32_RDMSJoinedNode
- Класс Win32_RDMSJoinedNode службы удаленных рабочих столов, метод Жетжоинеднодекаунт
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672615"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="9b4cd-106">Метод Жетжоинеднодекаунт \_ класса Win32 рдмсжоинедноде</span><span class="sxs-lookup"><span data-stu-id="9b4cd-106">GetJoinedNodeCount method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="9b4cd-107">Возвращает число серверов, на которых установлены указанные роли.</span><span class="sxs-lookup"><span data-stu-id="9b4cd-107">Get number of servers that have the specified roles installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b4cd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b4cd-108">Syntax</span></span>


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a><span data-ttu-id="9b4cd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b4cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b4cd-110">*roleType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9b4cd-110">*roleType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4cd-111">Битовое поле, указывающее типы ролей.</span><span class="sxs-lookup"><span data-stu-id="9b4cd-111">A bitfield that specifies the role types.</span></span>

<dt>

<span data-ttu-id="9b4cd-112">0</span><span class="sxs-lookup"><span data-stu-id="9b4cd-112">0</span></span>
</dt> <dd>

<span data-ttu-id="9b4cd-113">Все</span><span class="sxs-lookup"><span data-stu-id="9b4cd-113">All</span></span>

</dd> <dt>

<span data-ttu-id="9b4cd-114">1</span><span class="sxs-lookup"><span data-stu-id="9b4cd-114">1</span></span>
</dt> <dd>

<span data-ttu-id="9b4cd-115">Брокер подключение к удаленному рабочему столу (РДКБ)</span><span class="sxs-lookup"><span data-stu-id="9b4cd-115">Remote Desktop Connection Broker (RDCB)</span></span>

</dd> <dt>

<span data-ttu-id="9b4cd-116">2</span><span class="sxs-lookup"><span data-stu-id="9b4cd-116">2</span></span>
</dt> <dd>

<span data-ttu-id="9b4cd-117">Узел сеансов удаленный рабочий стол (узлов сеансов удаленных рабочих столов)</span><span class="sxs-lookup"><span data-stu-id="9b4cd-117">Remote Desktop Session Host (RDSH)</span></span>

</dd> <dt>

<span data-ttu-id="9b4cd-118">4</span><span class="sxs-lookup"><span data-stu-id="9b4cd-118">4</span></span>
</dt> <dd>

<span data-ttu-id="9b4cd-119">Узел виртуализации удаленных рабочих столов (РДВХ)</span><span class="sxs-lookup"><span data-stu-id="9b4cd-119">Remote Desktop Virtualization Host (RDVH)</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="9b4cd-120">*Количество* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9b4cd-120">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4cd-121">При успешном выполнении возвращает число серверов с установленными указанными ролями.</span><span class="sxs-lookup"><span data-stu-id="9b4cd-121">On success, returns the number of servers with the specified roles installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b4cd-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b4cd-122">Return value</span></span>

<span data-ttu-id="9b4cd-123">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="9b4cd-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b4cd-124">Требования</span><span class="sxs-lookup"><span data-stu-id="9b4cd-124">Requirements</span></span>



| <span data-ttu-id="9b4cd-125">Требование</span><span class="sxs-lookup"><span data-stu-id="9b4cd-125">Requirement</span></span> | <span data-ttu-id="9b4cd-126">Значение</span><span class="sxs-lookup"><span data-stu-id="9b4cd-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b4cd-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b4cd-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9b4cd-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9b4cd-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9b4cd-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b4cd-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9b4cd-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9b4cd-130">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="9b4cd-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9b4cd-131">Namespace</span></span><br/>                | <span data-ttu-id="9b4cd-132">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="9b4cd-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9b4cd-133">MOF</span><span class="sxs-lookup"><span data-stu-id="9b4cd-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b4cd-134"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b4cd-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b4cd-135">DLL</span><span class="sxs-lookup"><span data-stu-id="9b4cd-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b4cd-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b4cd-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9b4cd-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b4cd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b4cd-138">**\_Рдмсжоинедноде Win32**</span><span class="sxs-lookup"><span data-stu-id="9b4cd-138">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





