---
title: Метод Сетенаблед класса Win32_SessionDirectoryVMMPlugin
description: Включает или отключает подключаемый модуль.
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетенаблед
- Службы удаленных рабочих столов метода Сетенаблед, класс Win32_SessionDirectoryVMMPlugin
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов, метод Сетенаблед
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7089a21f143b6f3b27fe9fe58563e6777bf2f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803857"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="7d97c-106">Метод Сетенаблед \_ класса Win32 сессиондиректоривммплугин</span><span class="sxs-lookup"><span data-stu-id="7d97c-106">SetEnabled method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="7d97c-107">Включает или отключает подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="7d97c-107">Enables or disables the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d97c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d97c-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="7d97c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d97c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d97c-110">*Включено* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7d97c-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d97c-111">Указывает, включен ли или отключен подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="7d97c-111">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="7d97c-112">**Значение true** , если подключаемый модуль включен или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7d97c-112">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d97c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d97c-113">Return value</span></span>

<span data-ttu-id="7d97c-114">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="7d97c-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7d97c-115">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7d97c-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d97c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7d97c-116">Requirements</span></span>



| <span data-ttu-id="7d97c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7d97c-117">Requirement</span></span> | <span data-ttu-id="7d97c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7d97c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d97c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d97c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7d97c-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7d97c-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7d97c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d97c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7d97c-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7d97c-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="7d97c-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7d97c-123">Namespace</span></span><br/>                | <span data-ttu-id="7d97c-124">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="7d97c-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="7d97c-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7d97c-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d97c-126"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d97c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7d97c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d97c-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d97c-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d97c-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d97c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d97c-130">**\_Сессиондиректоривммплугин Win32**</span><span class="sxs-lookup"><span data-stu-id="7d97c-130">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





