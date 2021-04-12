---
title: Метод Жетпендингстартсерверлист класса Win32_RDSHServer
description: Возвращает список серверов, ожидающих запуска.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетпендингстартсерверлист
- Службы удаленных рабочих столов метода Жетпендингстартсерверлист, класс Win32_RDSHServer
- Класс Win32_RDSHServer службы удаленных рабочих столов, метод Жетпендингстартсерверлист
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415632"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="02f15-106">Метод Жетпендингстартсерверлист \_ класса Win32 рдшсервер</span><span class="sxs-lookup"><span data-stu-id="02f15-106">GetPendingStartServerList method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="02f15-107">Возвращает список серверов, ожидающих запуска.</span><span class="sxs-lookup"><span data-stu-id="02f15-107">Retrieves a list of server waiting to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f15-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02f15-108">Syntax</span></span>


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a><span data-ttu-id="02f15-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="02f15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02f15-110">*макссерверс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="02f15-110">*maxServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02f15-111">Максимальное число серверов, возвращаемых в списке.</span><span class="sxs-lookup"><span data-stu-id="02f15-111">The maximum number of servers to return in the list.</span></span>

</dd> <dt>

<span data-ttu-id="02f15-112">*Серверфкднс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="02f15-112">*ServerFQDNs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02f15-113">При успешном выполнении содержит коллекцию полных доменных имен серверов, ожидающих запуска.</span><span class="sxs-lookup"><span data-stu-id="02f15-113">On success, contains a collection of fully-qualified domain names of the servers waiting to start.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02f15-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02f15-114">Remarks</span></span>

<span data-ttu-id="02f15-115">Список серверов сбрасывается после каждого вызова, чтобы следующий вызов не получит дублирующий сервер.</span><span class="sxs-lookup"><span data-stu-id="02f15-115">The list of servers is reset after every call, so that the next call will not get a duplicate server.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f15-116">Требования</span><span class="sxs-lookup"><span data-stu-id="02f15-116">Requirements</span></span>



| <span data-ttu-id="02f15-117">Требование</span><span class="sxs-lookup"><span data-stu-id="02f15-117">Requirement</span></span> | <span data-ttu-id="02f15-118">Значение</span><span class="sxs-lookup"><span data-stu-id="02f15-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="02f15-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02f15-119">Minimum supported client</span></span><br/> | <span data-ttu-id="02f15-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="02f15-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="02f15-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02f15-121">Minimum supported server</span></span><br/> | <span data-ttu-id="02f15-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="02f15-122">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="02f15-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="02f15-123">Namespace</span></span><br/>                | <span data-ttu-id="02f15-124">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="02f15-124">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="02f15-125">MOF</span><span class="sxs-lookup"><span data-stu-id="02f15-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02f15-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02f15-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="02f15-127">DLL</span><span class="sxs-lookup"><span data-stu-id="02f15-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02f15-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02f15-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="02f15-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02f15-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f15-130">**\_Рдшсервер Win32**</span><span class="sxs-lookup"><span data-stu-id="02f15-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





