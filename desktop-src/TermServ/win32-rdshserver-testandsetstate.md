---
title: Метод Тестандсетстате класса Win32_RDSHServer
description: Сравнивает текущее состояние с указанным сравниваемый операнд; Если два совпадения, то для состояния задается новое значение. Независимо от соответствия, также возвращается текущее состояние.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Тестандсетстате
- Службы удаленных рабочих столов метода Тестандсетстате, класс Win32_RDSHServer
- Класс Win32_RDSHServer службы удаленных рабочих столов, метод Тестандсетстате
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136102"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="27621-107">Метод Тестандсетстате \_ класса Win32 рдшсервер</span><span class="sxs-lookup"><span data-stu-id="27621-107">TestAndSetState method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="27621-108">Сравнивает текущее состояние с указанным сравниваемый операнд; Если два совпадения, то для состояния задается новое значение.</span><span class="sxs-lookup"><span data-stu-id="27621-108">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="27621-109">Независимо от соответствия, также возвращается текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="27621-109">Regardless of the match, the current state is also returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="27621-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27621-110">Syntax</span></span>


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a><span data-ttu-id="27621-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="27621-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27621-112">*Сравниваемый операнд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27621-112">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27621-113">Значение, сравниваемое с текущим состоянием. Если два значения совпадают, то для состояния задается значение *NewState*.</span><span class="sxs-lookup"><span data-stu-id="27621-113">A value to compare to the current state; if the two values match, the state is set to *NewState*.</span></span>

</dd> <dt>

<span data-ttu-id="27621-114">*NewState* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27621-114">*NewState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27621-115">Новое значение состояния.</span><span class="sxs-lookup"><span data-stu-id="27621-115">The new value of the state.</span></span>

</dd> <dt>

<span data-ttu-id="27621-116">*Инитстате* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="27621-116">*InitState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="27621-117">При успешном или неудачном завершении возвращает текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="27621-117">On success or failure, returns the current state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27621-118">Требования</span><span class="sxs-lookup"><span data-stu-id="27621-118">Requirements</span></span>



| <span data-ttu-id="27621-119">Требование</span><span class="sxs-lookup"><span data-stu-id="27621-119">Requirement</span></span> | <span data-ttu-id="27621-120">Значение</span><span class="sxs-lookup"><span data-stu-id="27621-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="27621-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27621-121">Minimum supported client</span></span><br/> | <span data-ttu-id="27621-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="27621-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="27621-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27621-123">Minimum supported server</span></span><br/> | <span data-ttu-id="27621-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="27621-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="27621-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="27621-125">Namespace</span></span><br/>                | <span data-ttu-id="27621-126">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="27621-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="27621-127">MOF</span><span class="sxs-lookup"><span data-stu-id="27621-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="27621-128"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="27621-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="27621-129">DLL</span><span class="sxs-lookup"><span data-stu-id="27621-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27621-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27621-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="27621-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27621-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27621-132">**\_Рдшсервер Win32**</span><span class="sxs-lookup"><span data-stu-id="27621-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





