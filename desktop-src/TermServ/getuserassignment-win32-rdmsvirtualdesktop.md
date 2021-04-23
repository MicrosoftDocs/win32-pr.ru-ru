---
title: Метод Жетусерассигнмент класса Win32_RDMSVirtualDesktop
description: Получение имени пользователя и домена пользователя, назначенного виртуальному рабочему столу.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетусерассигнмент
- Службы удаленных рабочих столов метода Жетусерассигнмент, класс Win32_RDMSVirtualDesktop
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов, метод Жетусерассигнмент
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87293a471bb4f69b3f4c57de0f964fa0daa043cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415776"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="acdf5-106">Метод Жетусерассигнмент \_ класса Win32 рдмсвиртуалдесктоп</span><span class="sxs-lookup"><span data-stu-id="acdf5-106">GetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="acdf5-107">Получение имени пользователя и домена пользователя, назначенного виртуальному рабочему столу.</span><span class="sxs-lookup"><span data-stu-id="acdf5-107">Retrieves the username and domain name of the user that is assigned to the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="acdf5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acdf5-108">Syntax</span></span>


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="acdf5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="acdf5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acdf5-110">*Имя пользователя* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="acdf5-110">*UserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acdf5-111">Получает имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="acdf5-111">Receives the username.</span></span>

</dd> <dt>

<span data-ttu-id="acdf5-112">*Доменпользователя* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="acdf5-112">*UserDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acdf5-113">Получает доменное имя.</span><span class="sxs-lookup"><span data-stu-id="acdf5-113">Receives the domain name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acdf5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acdf5-114">Return value</span></span>

<span data-ttu-id="acdf5-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="acdf5-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="acdf5-116">Требования</span><span class="sxs-lookup"><span data-stu-id="acdf5-116">Requirements</span></span>



| <span data-ttu-id="acdf5-117">Требование</span><span class="sxs-lookup"><span data-stu-id="acdf5-117">Requirement</span></span> | <span data-ttu-id="acdf5-118">Значение</span><span class="sxs-lookup"><span data-stu-id="acdf5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="acdf5-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acdf5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="acdf5-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="acdf5-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="acdf5-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acdf5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="acdf5-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="acdf5-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="acdf5-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="acdf5-123">Namespace</span></span><br/>                | <span data-ttu-id="acdf5-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="acdf5-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="acdf5-125">MOF</span><span class="sxs-lookup"><span data-stu-id="acdf5-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acdf5-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acdf5-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="acdf5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="acdf5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acdf5-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acdf5-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="acdf5-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acdf5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acdf5-130">**\_Рдмсвиртуалдесктоп Win32**</span><span class="sxs-lookup"><span data-stu-id="acdf5-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





