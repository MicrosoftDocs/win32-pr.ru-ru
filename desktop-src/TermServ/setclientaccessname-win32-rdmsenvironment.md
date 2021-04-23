---
title: Метод Сетклиентакцесснаме класса Win32_RDMSEnvironment
description: Обновляет имя записи ресурса службы доменных имен (DNS) в среде служб управления удаленный рабочий стол (RDMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетклиентакцесснаме
- Службы удаленных рабочих столов метода Сетклиентакцесснаме, класс Win32_RDMSEnvironment
- Класс Win32_RDMSEnvironment службы удаленных рабочих столов, метод Сетклиентакцесснаме
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f9087fe2c2139833baeb21bc62da508c6e5989
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672872"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a><span data-ttu-id="59928-106">Метод Сетклиентакцесснаме \_ класса Win32 рдмсенвиронмент</span><span class="sxs-lookup"><span data-stu-id="59928-106">SetClientAccessName method of the Win32\_RDMSEnvironment class</span></span>

<span data-ttu-id="59928-107">Обновляет имя записи ресурса службы доменных имен (DNS) в среде служб управления удаленный рабочий стол (RDMS).</span><span class="sxs-lookup"><span data-stu-id="59928-107">Updates the Domain Name System (DNS) resource record (RR) name of an Remote Desktop Management Services (RDMS) environment.</span></span>

## <a name="syntax"></a><span data-ttu-id="59928-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59928-108">Syntax</span></span>


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a><span data-ttu-id="59928-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="59928-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59928-110">*Клиентакцесснаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="59928-110">*ClientAccessName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59928-111">Новое имя записи ресурса.</span><span class="sxs-lookup"><span data-stu-id="59928-111">The new RR name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59928-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="59928-112">Return value</span></span>

<span data-ttu-id="59928-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="59928-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="59928-114">Требования</span><span class="sxs-lookup"><span data-stu-id="59928-114">Requirements</span></span>



| <span data-ttu-id="59928-115">Требование</span><span class="sxs-lookup"><span data-stu-id="59928-115">Requirement</span></span> | <span data-ttu-id="59928-116">Значение</span><span class="sxs-lookup"><span data-stu-id="59928-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="59928-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59928-117">Minimum supported client</span></span><br/> | <span data-ttu-id="59928-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="59928-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="59928-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59928-119">Minimum supported server</span></span><br/> | <span data-ttu-id="59928-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="59928-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="59928-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="59928-121">Namespace</span></span><br/>                | <span data-ttu-id="59928-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="59928-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="59928-123">MOF</span><span class="sxs-lookup"><span data-stu-id="59928-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59928-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59928-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="59928-125">DLL</span><span class="sxs-lookup"><span data-stu-id="59928-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59928-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59928-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="59928-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59928-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59928-128">**\_Рдмсенвиронмент Win32**</span><span class="sxs-lookup"><span data-stu-id="59928-128">**Win32\_RDMSEnvironment**</span></span>](win32-rdmsenvironment.md)
</dt> </dl>

 

 





