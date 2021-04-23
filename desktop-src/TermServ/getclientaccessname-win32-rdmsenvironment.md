---
title: Метод Жетклиентакцесснаме класса Win32_RDMSEnvironment
description: Извлекает имя записи ресурса службы доменных имен (DNS) для среды управления удаленный рабочий стол (RDMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетклиентакцесснаме
- Службы удаленных рабочих столов метода Жетклиентакцесснаме, класс Win32_RDMSEnvironment
- Класс Win32_RDMSEnvironment службы удаленных рабочих столов, метод Жетклиентакцесснаме
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f54662cf1f27c53f3bf69398a203bfdfce1e53c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681776"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="cc214-106">Метод Жетклиентакцесснаме \_ класса Win32 рдмсенвиронмент</span><span class="sxs-lookup"><span data-stu-id="cc214-106">GetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="cc214-107">Извлекает имя записи ресурса службы доменных имен (DNS) для среды управления удаленный рабочий стол (RDMS).</span><span class="sxs-lookup"><span data-stu-id="cc214-107">Retrieves the Domain Name System (DNS) resource record (RR) name of the Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc214-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc214-108">Syntax</span></span>


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="cc214-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc214-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc214-110">*Клиентакцесснаме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="cc214-110">*ClientAccessName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc214-111">Получает полученное имя записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc214-111">Receives the retrieved RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc214-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cc214-112">Return value</span></span>

<span data-ttu-id="cc214-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="cc214-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc214-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cc214-114">Requirements</span></span>



| <span data-ttu-id="cc214-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cc214-115">Requirement</span></span> | <span data-ttu-id="cc214-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cc214-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc214-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc214-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc214-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cc214-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cc214-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc214-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc214-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cc214-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="cc214-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cc214-121">Namespace</span></span><br/>                | <span data-ttu-id="cc214-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="cc214-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cc214-123">MOF</span><span class="sxs-lookup"><span data-stu-id="cc214-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc214-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc214-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc214-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cc214-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc214-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc214-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cc214-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc214-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc214-128">**\_Рдмсенвиронмент Win32**</span><span class="sxs-lookup"><span data-stu-id="cc214-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





