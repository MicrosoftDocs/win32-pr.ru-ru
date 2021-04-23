---
description: Функция Инсталлвиадевице устанавливает устройство для получения образа Windows (WIA) в качестве устройства с корневым перечислением. Это может привести к появлении предупреждения системы безопасности, если любой устанавливаемый файл или установщик не имеют цифровой подписи и не являются доверенными.
ms.assetid: c7de27f5-5994-4fce-a6ec-6e7cfae2e591
title: Функция Инсталлвиадевице (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallWiaDevice
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 62060d538b4b51fe22e10df09093f1f7f8c26a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810798"
---
# <a name="installwiadevice-function"></a><span data-ttu-id="e3589-104">Функция Инсталлвиадевице</span><span class="sxs-lookup"><span data-stu-id="e3589-104">InstallWiaDevice function</span></span>

<span data-ttu-id="e3589-105">Функция **инсталлвиадевице** устанавливает устройство для получения образа Windows (WIA) в качестве устройства с корневым перечислением.</span><span class="sxs-lookup"><span data-stu-id="e3589-105">The **InstallWiaDevice** function installs a Windows Image Acquisition (WIA) device as root-enumerated device.</span></span> <span data-ttu-id="e3589-106">Это может привести к появлении предупреждения системы безопасности, если любой устанавливаемый файл или установщик не имеют цифровой подписи и не являются доверенными.</span><span class="sxs-lookup"><span data-stu-id="e3589-106">It may popup a security warning if any installing file or coinstaller is not digitally signed and trusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3589-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3589-107">Syntax</span></span>


```C++
DWORD WINAPI InstallWiaDevice(
  _In_ PWIADEVICEINSTALL *pWiaDeviceInstall
);
```



## <a name="parameters"></a><span data-ttu-id="e3589-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3589-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3589-109">*пвиадевицеинсталл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e3589-109">*pWiaDeviceInstall* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3589-110">Тип: \**пвиадевицеинсталл \** _</span><span class="sxs-lookup"><span data-stu-id="e3589-110">Type: \**PWIADEVICEINSTALL\** _</span></span>

<span data-ttu-id="e3589-111">Указатель на структуру ВИАДЕВИЦЕИНСТАЛЛ.</span><span class="sxs-lookup"><span data-stu-id="e3589-111">Pointer to a WIADEVICEINSTALL structure.</span></span> <span data-ttu-id="e3589-112">Для элемента _szFriendlyName \* структуры необходимо задать фактическое значение FriendlyName для устройства.</span><span class="sxs-lookup"><span data-stu-id="e3589-112">The _szFriendlyName\* member of the structure must be set to the actual device FriendlyName.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3589-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3589-113">Return value</span></span>

<span data-ttu-id="e3589-114">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="e3589-114">Type: **DWORD**</span></span>

<span data-ttu-id="e3589-115">Если функция завершается успешно, возвращается значение ошибки \_ Success.</span><span class="sxs-lookup"><span data-stu-id="e3589-115">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="e3589-116">Если функция завершается ошибкой, возвращается код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="e3589-116">If the function fails, it returns a Win32 error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3589-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e3589-117">Requirements</span></span>



| <span data-ttu-id="e3589-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e3589-118">Requirement</span></span> | <span data-ttu-id="e3589-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e3589-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3589-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e3589-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3589-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e3589-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e3589-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e3589-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3589-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e3589-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e3589-124">Header</span><span class="sxs-lookup"><span data-stu-id="e3589-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3589-125"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3589-125"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="e3589-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e3589-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3589-127"><dt>Виагуид. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3589-127"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




