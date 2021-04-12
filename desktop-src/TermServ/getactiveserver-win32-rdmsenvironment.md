---
title: Метод Жетактивесервер класса Win32_RDMSEnvironment
description: Получает полное доменное имя (FQDN) среды служб управления удаленный рабочий стол (RDMS).
ms.assetid: 87e25d11-de1d-41d1-974d-2871dde444b5
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетактивесервер
- Службы удаленных рабочих столов метода Жетактивесервер, класс Win32_RDMSEnvironment
- Класс Win32_RDMSEnvironment службы удаленных рабочих столов, метод Жетактивесервер
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetActiveServer
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4265315e3ed2de87e564adab87c023401bbd55e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491349"
---
# <a name="getactiveserver-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="fe605-106">Метод Жетактивесервер \_ класса Win32 рдмсенвиронмент</span><span class="sxs-lookup"><span data-stu-id="fe605-106">GetActiveServer method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="fe605-107">Получает полное доменное имя (FQDN) среды служб управления удаленный рабочий стол (RDMS).</span><span class="sxs-lookup"><span data-stu-id="fe605-107">Retrieves the fully qualified domain name (FQDN) of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe605-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe605-108">Syntax</span></span>


```mof
uint32 GetActiveServer(
  [out] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="fe605-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe605-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe605-110">*Имя сервера* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fe605-110">*ServerName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe605-111">Получает полученное полное доменное имя.</span><span class="sxs-lookup"><span data-stu-id="fe605-111">Receives the retrieved FQDN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe605-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe605-112">Return value</span></span>

<span data-ttu-id="fe605-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="fe605-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe605-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fe605-114">Requirements</span></span>



| <span data-ttu-id="fe605-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fe605-115">Requirement</span></span> | <span data-ttu-id="fe605-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fe605-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe605-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe605-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fe605-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fe605-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fe605-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe605-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fe605-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fe605-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fe605-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fe605-121">Namespace</span></span><br/>                | <span data-ttu-id="fe605-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="fe605-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fe605-123">MOF</span><span class="sxs-lookup"><span data-stu-id="fe605-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe605-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe605-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe605-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fe605-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe605-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe605-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fe605-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe605-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe605-128">**\_Рдмсенвиронмент Win32**</span><span class="sxs-lookup"><span data-stu-id="fe605-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





