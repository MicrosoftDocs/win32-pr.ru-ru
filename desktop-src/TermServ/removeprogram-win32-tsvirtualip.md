---
title: Метод Ремовепрограм класса Win32_TSVirtualIP (Бдаифаце. h)
description: Удаляет программу из списка программ, использующих виртуализацию IP-адресов.
ms.assetid: 2a8069a0-2c48-40d3-a850-0cdfce4fbc82
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовепрограм
- Службы удаленных рабочих столов метода Ремовепрограм, класс Win32_TSVirtualIP
- Класс Win32_TSVirtualIP службы удаленных рабочих столов, метод Ремовепрограм
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.RemoveProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6241664b6e56c3d387673b6a1cc50e43b413336
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803869"
---
# <a name="removeprogram-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="a768e-106">Метод Ремовепрограм \_ класса Win32 тсвиртуалип</span><span class="sxs-lookup"><span data-stu-id="a768e-106">RemoveProgram method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="a768e-107">Удаляет программу из списка программ, использующих виртуализацию IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="a768e-107">Removes a program from the list of programs that use IP virtualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="a768e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a768e-108">Syntax</span></span>


```mof
uint32 RemoveProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a><span data-ttu-id="a768e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a768e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a768e-110">*Програмпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a768e-110">*ProgramPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a768e-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="a768e-111">Type: **string**</span></span>

<span data-ttu-id="a768e-112">Путь и имя файла программы, которую необходимо удалить из списка.</span><span class="sxs-lookup"><span data-stu-id="a768e-112">The path and file name of the program to remove from the list.</span></span> <span data-ttu-id="a768e-113">Если программа не найдена, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="a768e-113">If the program is not found, an error is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a768e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a768e-114">Return value</span></span>

<span data-ttu-id="a768e-115">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a768e-115">Type: **uint32**</span></span>

<span data-ttu-id="a768e-116">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="a768e-116">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a768e-117">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a768e-117">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a768e-118">Метод возвращает ошибку, если параметр находится в разделе Управление групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="a768e-118">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a768e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a768e-119">Requirements</span></span>



| <span data-ttu-id="a768e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a768e-120">Requirement</span></span> | <span data-ttu-id="a768e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a768e-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a768e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a768e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a768e-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a768e-123">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a768e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a768e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a768e-125">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a768e-125">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a768e-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a768e-126">Namespace</span></span><br/>                | <span data-ttu-id="a768e-127">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a768e-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a768e-128">Header</span><span class="sxs-lookup"><span data-stu-id="a768e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a768e-129"><dt>Бдаифаце. h</dt></span><span class="sxs-lookup"><span data-stu-id="a768e-129"><dt>Bdaiface.h</dt></span></span> </dl>   |
| <span data-ttu-id="a768e-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a768e-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a768e-131"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a768e-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a768e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a768e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a768e-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a768e-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a768e-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a768e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a768e-135">**\_Тсвиртуалип Win32**</span><span class="sxs-lookup"><span data-stu-id="a768e-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





