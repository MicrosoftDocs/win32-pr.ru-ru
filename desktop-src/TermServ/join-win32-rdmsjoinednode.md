---
title: Метод join класса Win32_RDMSJoinedNode
description: Добавляет узел в службы удаленный рабочий стол Management Services (RDMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Join
- Метод Join службы удаленных рабочих столов, класс Win32_RDMSJoinedNode
- Класс Win32_RDMSJoinedNode службы удаленных рабочих столов, метод Join
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415029"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="3dc82-106">Метод Join \_ класса Рдмсжоинедноде Win32</span><span class="sxs-lookup"><span data-stu-id="3dc82-106">Join method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="3dc82-107">Добавляет узел в службы удаленный рабочий стол Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="3dc82-107">Adds a node to Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="3dc82-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3dc82-108">Syntax</span></span>


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a><span data-ttu-id="3dc82-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3dc82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dc82-110">*Нодефкдн* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3dc82-110">*NodeFQDN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc82-111">Полное доменное имя узла.</span><span class="sxs-lookup"><span data-stu-id="3dc82-111">The fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="3dc82-112">*Нодесид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3dc82-112">*NodeSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dc82-113">Идентификатор безопасности (SID) узла.</span><span class="sxs-lookup"><span data-stu-id="3dc82-113">The security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dc82-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3dc82-114">Return value</span></span>

<span data-ttu-id="3dc82-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="3dc82-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dc82-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3dc82-116">Requirements</span></span>



| <span data-ttu-id="3dc82-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3dc82-117">Requirement</span></span> | <span data-ttu-id="3dc82-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3dc82-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dc82-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3dc82-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3dc82-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3dc82-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3dc82-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3dc82-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3dc82-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3dc82-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="3dc82-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3dc82-123">Namespace</span></span><br/>                | <span data-ttu-id="3dc82-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="3dc82-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3dc82-125">MOF</span><span class="sxs-lookup"><span data-stu-id="3dc82-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dc82-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3dc82-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3dc82-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3dc82-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dc82-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dc82-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3dc82-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3dc82-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dc82-130">**\_Рдмсжоинедноде Win32**</span><span class="sxs-lookup"><span data-stu-id="3dc82-130">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





