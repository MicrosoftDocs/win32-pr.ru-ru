---
description: Возвращает сведения о версии текущей работающей операционной системы.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Функция Ртлжетверсион (Нтддк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: a6a026ee55a6ccd75162915729070ad76f621bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141255"
---
# <a name="rtlgetversion-function"></a><span data-ttu-id="3c2e9-103">Функция Ртлжетверсион</span><span class="sxs-lookup"><span data-stu-id="3c2e9-103">RtlGetVersion function</span></span>

<span data-ttu-id="3c2e9-104">Возвращает сведения о версии текущей работающей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3c2e9-104">Gets version information about the currently running operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c2e9-105">Syntax</span></span>


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a><span data-ttu-id="3c2e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c2e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c2e9-107">*лпверсионинформатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="3c2e9-107">*lpVersionInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2e9-108">Указатель на структуру [**\_ осверсионинфов справа налево**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) или структуру [**\_ осверсионинфоексв RTL**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) , содержащую сведения о версии текущей операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3c2e9-108">Pointer to either a [**RTL\_OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) structure or a [**RTL\_OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) structure that contains the version information about the currently running operating system.</span></span> <span data-ttu-id="3c2e9-109">Вызывающий объект указывает, какая структура ввода используется, устанавливая для элемента **двосверсионинфосизе** структуры размер в байтах используемой структуры.</span><span class="sxs-lookup"><span data-stu-id="3c2e9-109">A caller specifies which input structure is used by setting the **dwOSVersionInfoSize** member of the structure to the size in bytes of the structure that is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c2e9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c2e9-110">Return value</span></span>

<span data-ttu-id="3c2e9-111">Возвращает состояние \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3c2e9-111">Returns STATUS\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c2e9-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c2e9-112">Remarks</span></span>

<span data-ttu-id="3c2e9-113">**Ртлжетверсион** является эквивалентом функции [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3c2e9-113">**RtlGetVersion** is the equivalent of the [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) function in the Windows SDK.</span></span> <span data-ttu-id="3c2e9-114">См. пример в Windows SDK, в котором показано, как получить версию системы.</span><span class="sxs-lookup"><span data-stu-id="3c2e9-114">See the example in the Windows SDK that shows how to get the system version.</span></span>

<span data-ttu-id="3c2e9-115">При использовании **ртлжетверсион** для определения того, запущена ли определенная версия операционной системы, вызывающая сторона должна проверить номера версий, которые больше или равны номеру требуемой версии.</span><span class="sxs-lookup"><span data-stu-id="3c2e9-115">When using **RtlGetVersion** to determine whether a particular version of the operating system is running, a caller should check for version numbers that are greater than or equal to the required version number.</span></span> <span data-ttu-id="3c2e9-116">Это гарантирует, что тест версии будет выполнен для более поздних версий Windows.</span><span class="sxs-lookup"><span data-stu-id="3c2e9-116">This ensures that a version test succeeds for later versions of Windows.</span></span>

<span data-ttu-id="3c2e9-117">Поскольку функции операционной системы могут быть добавлены в распространяемую библиотеку DLL, проверка только основного и дополнительного номеров версий не является самым надежным способом проверки наличия определенного компонента системы.</span><span class="sxs-lookup"><span data-stu-id="3c2e9-117">Because operating system features can be added in a redistributable DLL, checking only the major and minor version numbers is not the most reliable way to verify the presence of a specific system feature.</span></span> <span data-ttu-id="3c2e9-118">Драйвер должен использовать [**ртлверифиверсионинфо**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) для проверки наличия определенного компонента системы.</span><span class="sxs-lookup"><span data-stu-id="3c2e9-118">A driver should use [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) to test for the presence of a specific system feature.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2e9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3c2e9-119">Requirements</span></span>



| <span data-ttu-id="3c2e9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3c2e9-120">Requirement</span></span> | <span data-ttu-id="3c2e9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3c2e9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2e9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c2e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2e9-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c2e9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="3c2e9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c2e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2e9-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3c2e9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="3c2e9-126">Целевая платформа</span><span class="sxs-lookup"><span data-stu-id="3c2e9-126">Target platform</span></span><br/>          | <dl> <span data-ttu-id="3c2e9-127"><dt>[Универсальной](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="3c2e9-127"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl>                  |
| <span data-ttu-id="3c2e9-128">Header</span><span class="sxs-lookup"><span data-stu-id="3c2e9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c2e9-129"><dt>Нтддк. h (включение Нтддк. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3c2e9-129"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                                     |
| <span data-ttu-id="3c2e9-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="3c2e9-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c2e9-131"><dt>NTDLL. lib; </dt> <dt>NtosKrnl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c2e9-131"><dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c2e9-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3c2e9-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c2e9-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3c2e9-133"><dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c2e9-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c2e9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2e9-135">**псжетверсион**</span><span class="sxs-lookup"><span data-stu-id="3c2e9-135">**PsGetVersion**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
