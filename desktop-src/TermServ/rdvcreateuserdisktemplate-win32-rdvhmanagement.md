---
title: Метод Рдвкреатеусердисктемплате класса Win32_RdvhManagement
description: Создает пользовательский шаблон диска с указанным максимальным размером в указанном расположении.
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рдвкреатеусердисктемплате
- Службы удаленных рабочих столов метода Рдвкреатеусердисктемплате, класс Win32_RdvhManagement
- Класс Win32_RdvhManagement службы удаленных рабочих столов, метод Рдвкреатеусердисктемплате
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803616"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="f543a-106">Метод Рдвкреатеусердисктемплате \_ класса Win32 рдвхманажемент</span><span class="sxs-lookup"><span data-stu-id="f543a-106">RdvCreateUserDiskTemplate method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="f543a-107">Создает пользовательский шаблон диска с указанным максимальным размером в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="f543a-107">Creates a user disk template, with the specified maximum size, at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="f543a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f543a-108">Syntax</span></span>


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="f543a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f543a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f543a-110">*Усердискссторажеурл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f543a-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f543a-111">Расположение дискового пространства пользователя.</span><span class="sxs-lookup"><span data-stu-id="f543a-111">Location of the user disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="f543a-112">*Усердискмакссизеингб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f543a-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f543a-113">Максимальный размер диска пользователя в ГБ.</span><span class="sxs-lookup"><span data-stu-id="f543a-113">Maximum size of the user disk, in GB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f543a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f543a-114">Return value</span></span>

<span data-ttu-id="f543a-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="f543a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f543a-116">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f543a-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f543a-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f543a-117">Remarks</span></span>

<span data-ttu-id="f543a-118">Все диски пользователей, созданные с помощью этого шаблона, будут иметь тот же максимальный размер, что и шаблон.</span><span class="sxs-lookup"><span data-stu-id="f543a-118">All user disks created using this template will have the same maximum size as the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="f543a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f543a-119">Requirements</span></span>



| <span data-ttu-id="f543a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f543a-120">Requirement</span></span> | <span data-ttu-id="f543a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f543a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f543a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f543a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f543a-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f543a-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="f543a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f543a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f543a-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f543a-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="f543a-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f543a-126">Namespace</span></span><br/>                | <span data-ttu-id="f543a-127">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="f543a-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="f543a-128">MOF</span><span class="sxs-lookup"><span data-stu-id="f543a-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f543a-129"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f543a-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="f543a-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f543a-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f543a-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f543a-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f543a-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f543a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f543a-133">**\_Рдвхманажемент Win32**</span><span class="sxs-lookup"><span data-stu-id="f543a-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





