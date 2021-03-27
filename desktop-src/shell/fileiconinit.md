---
description: Инициализирует или повторно инициализирует список системных образов.
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: Функция Филеиконинит
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345415"
---
# <a name="fileiconinit-function"></a><span data-ttu-id="dc106-103">Функция Филеиконинит</span><span class="sxs-lookup"><span data-stu-id="dc106-103">FileIconInit function</span></span>

<span data-ttu-id="dc106-104">Инициализирует или повторно инициализирует список системных образов.</span><span class="sxs-lookup"><span data-stu-id="dc106-104">Initializes or reinitializes the system image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc106-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc106-105">Syntax</span></span>


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a><span data-ttu-id="dc106-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc106-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc106-107">*фресторекаче* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc106-107">*fRestoreCache* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc106-108">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="dc106-108">Type: **BOOL**</span></span>

<span data-ttu-id="dc106-109">**Значение true** , чтобы восстановить кэш образа системы с диска; В противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="dc106-109">**TRUE** to restore the system image cache from disk; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc106-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc106-110">Return value</span></span>

<span data-ttu-id="dc106-111">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="dc106-111">Type: **BOOL**</span></span>

<span data-ttu-id="dc106-112">**Значение true** , если кэш успешно обновлен, и **false** в случае сбоя инициализации.</span><span class="sxs-lookup"><span data-stu-id="dc106-112">**TRUE** if the cache was successfully refreshed, **FALSE** if the initialization failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc106-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="dc106-113">Remarks</span></span>

<span data-ttu-id="dc106-114">Если вы используете списки системных образов в собственном процессе, необходимо вызвать **филеиконинит** в следующее время:</span><span class="sxs-lookup"><span data-stu-id="dc106-114">If you are using system image lists in your own process, you must call **FileIconInit** at the following times:</span></span>

-   <span data-ttu-id="dc106-115">При запуске.</span><span class="sxs-lookup"><span data-stu-id="dc106-115">On launch.</span></span>
-   <span data-ttu-id="dc106-116">В ответ на сообщение [**\_ сеттингчанже WM**](../winmsg/wm-settingchange.md) , если установлен [**флаг \_ SPI сетнонклиентметрикс**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="dc106-116">In response to a [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message when the [**SPI\_SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) flag is set.</span></span>

<span data-ttu-id="dc106-117">**Филеиконинит** не включается в заголовочный файл.</span><span class="sxs-lookup"><span data-stu-id="dc106-117">**FileIconInit** is not included in a header file.</span></span> <span data-ttu-id="dc106-118">Его необходимо вызвать непосредственно из Shell32.dll с использованием порядкового номера 660.</span><span class="sxs-lookup"><span data-stu-id="dc106-118">You must call it directly from Shell32.dll, using ordinal 660.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc106-119">Требования</span><span class="sxs-lookup"><span data-stu-id="dc106-119">Requirements</span></span>



| <span data-ttu-id="dc106-120">Требование</span><span class="sxs-lookup"><span data-stu-id="dc106-120">Requirement</span></span> | <span data-ttu-id="dc106-121">Значение</span><span class="sxs-lookup"><span data-stu-id="dc106-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc106-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc106-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dc106-123">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dc106-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dc106-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc106-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dc106-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dc106-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dc106-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dc106-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc106-127"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc106-127"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
