---
title: Метод Delete класса Win32_TSAccount
description: Метод Delete удаляет указанную учетную запись пользователя, группы или компьютера.
ms.assetid: d0bb06d6-781c-4711-a59d-9ff233dd2a4c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Delete
- Службы удаленных рабочих столов метода Delete, класс Win32_TSAccount
- Класс Win32_TSAccount службы удаленных рабочих столов, метод Delete
topic_type:
- apiref
api_name:
- Win32_TSAccount.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ab76ad1200fc872a3a105e74533460104d806
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416029"
---
# <a name="delete-method-of-the-win32_tsaccount-class"></a><span data-ttu-id="7fd1e-106">Метод DELETE \_ класса Тсаккаунт Win32</span><span class="sxs-lookup"><span data-stu-id="7fd1e-106">Delete method of the Win32\_TSAccount class</span></span>

<span data-ttu-id="7fd1e-107">Метод **Delete** удаляет указанную учетную запись пользователя, группы или компьютера.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-107">The **Delete** method deletes the specified user, group, or computer account.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd1e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fd1e-108">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="7fd1e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fd1e-109">Parameters</span></span>

<span data-ttu-id="7fd1e-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7fd1e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fd1e-111">Return value</span></span>

<span data-ttu-id="7fd1e-112">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7fd1e-113">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7fd1e-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="7fd1e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fd1e-114">Remarks</span></span>

<span data-ttu-id="7fd1e-115">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7fd1e-115">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7fd1e-116">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="7fd1e-116">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7fd1e-117">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7fd1e-117">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7fd1e-118">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="7fd1e-118">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd1e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="7fd1e-119">Requirements</span></span>



| <span data-ttu-id="7fd1e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="7fd1e-120">Requirement</span></span> | <span data-ttu-id="7fd1e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="7fd1e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd1e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fd1e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd1e-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fd1e-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7fd1e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fd1e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd1e-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fd1e-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7fd1e-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7fd1e-126">Namespace</span></span><br/>                | <span data-ttu-id="7fd1e-127">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="7fd1e-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7fd1e-128">MOF</span><span class="sxs-lookup"><span data-stu-id="7fd1e-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fd1e-129"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fd1e-129"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fd1e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7fd1e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fd1e-131"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fd1e-131"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fd1e-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fd1e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd1e-133">**\_Тсаккаунт Win32**</span><span class="sxs-lookup"><span data-stu-id="7fd1e-133">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> </dl>

 

