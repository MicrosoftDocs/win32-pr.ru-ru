---
title: Метод Revoke класса Win32_TSIssuedLicense
description: Отменяет лицензию на клиентский доступ службы удаленных рабочих столов на устройство (RDS \ 160; CAL "на устройство"), представленные \_ объектом Win32 тсиссуедлиценсе. Это не статическая функция.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Отозвать метод службы удаленных рабочих столов
- Метод Revoke службы удаленных рабочих столов, Win32_TSIssuedLicense класс
- Win32_TSIssuedLicense класс службы удаленных рабочих столов, метод REVOKE
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803868"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a><span data-ttu-id="37e2b-107">Метод Revoke \_ класса Win32 тсиссуедлиценсе</span><span class="sxs-lookup"><span data-stu-id="37e2b-107">Revoke method of the Win32\_TSIssuedLicense class</span></span>

<span data-ttu-id="37e2b-108">Отменяет клиентские лицензии службы удаленных рабочих столов на устройство (CAL для устройств RDS), представленные объектом [**Win32 \_ тсиссуедлиценсе**](win32-tsissuedlicense.md) .</span><span class="sxs-lookup"><span data-stu-id="37e2b-108">Revokes the Remote Desktop Services Per Device client access licenses (RDS Per Device CALs) that are represented by the [**Win32\_TSIssuedLicense**](win32-tsissuedlicense.md) object.</span></span> <span data-ttu-id="37e2b-109">Это не статическая функция.</span><span class="sxs-lookup"><span data-stu-id="37e2b-109">This is not a static function.</span></span>

## <a name="syntax"></a><span data-ttu-id="37e2b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="37e2b-110">Syntax</span></span>


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a><span data-ttu-id="37e2b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="37e2b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37e2b-112">*Ревокаблекалс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="37e2b-112">*RevokableCals* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37e2b-113">Количество клиентских лицензий служб удаленных рабочих столов того же типа, что и текущий объект, который можно отозвать.</span><span class="sxs-lookup"><span data-stu-id="37e2b-113">Number of RDS CALs of the same type as the current object that can be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="37e2b-114">*Некстревокеалловедон* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="37e2b-114">*NextRevokeAllowedOn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37e2b-115">Дата, с которой администратор может далее попытаться отозвать лицензии.</span><span class="sxs-lookup"><span data-stu-id="37e2b-115">Date that the administrator can next try to revoke licenses.</span></span> <span data-ttu-id="37e2b-116">Этот параметр содержит только допустимые данные, если не удалось вызвать метод **REVOKE** , так как достигнуто максимальное число отмен.</span><span class="sxs-lookup"><span data-stu-id="37e2b-116">This parameter only contains valid data when the **Revoke** method call has failed because the maximum revoke count has been reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37e2b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="37e2b-117">Remarks</span></span>

<span data-ttu-id="37e2b-118">Для вызова этого метода необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="37e2b-118">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="37e2b-119">Можно отозвать только клиентские лицензии RDS "на устройство".</span><span class="sxs-lookup"><span data-stu-id="37e2b-119">Only RDS Per Device CALs can be revoked.</span></span>

<span data-ttu-id="37e2b-120">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="37e2b-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="37e2b-121">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="37e2b-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="37e2b-122">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="37e2b-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="37e2b-123">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="37e2b-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="37e2b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="37e2b-124">Requirements</span></span>



| <span data-ttu-id="37e2b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="37e2b-125">Requirement</span></span> | <span data-ttu-id="37e2b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="37e2b-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e2b-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="37e2b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="37e2b-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="37e2b-128">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="37e2b-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="37e2b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="37e2b-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37e2b-130">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="37e2b-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="37e2b-131">Namespace</span></span><br/>                | <span data-ttu-id="37e2b-132">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="37e2b-132">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="37e2b-133">MOF</span><span class="sxs-lookup"><span data-stu-id="37e2b-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37e2b-134"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37e2b-134"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="37e2b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="37e2b-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37e2b-136"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37e2b-136"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37e2b-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="37e2b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37e2b-138">**\_Тсиссуедлиценсе Win32**</span><span class="sxs-lookup"><span data-stu-id="37e2b-138">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> </dl>

 

