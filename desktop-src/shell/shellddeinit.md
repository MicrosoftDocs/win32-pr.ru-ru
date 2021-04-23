---
description: Регистрирует службы оболочки платформа динамических данных Exchange (DDE) в текущем процессе, уведомляя систему о том, что текущему процессу требуется разместить объекты DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: Функция Шеллддеинит
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985881"
---
# <a name="shellddeinit-function"></a><span data-ttu-id="83be2-103">Функция Шеллддеинит</span><span class="sxs-lookup"><span data-stu-id="83be2-103">ShellDDEInit function</span></span>

<span data-ttu-id="83be2-104">Регистрирует службы оболочки платформа динамических данных Exchange (DDE) в текущем процессе, уведомляя систему о том, что текущему процессу требуется разместить объекты DDE.</span><span class="sxs-lookup"><span data-stu-id="83be2-104">Registers the Shell Dynamic Data Exchange (DDE) services in the current process, notifying the system that the current process wishes to host DDE objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="83be2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="83be2-105">Syntax</span></span>


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a><span data-ttu-id="83be2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83be2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83be2-107">*Инициализация* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="83be2-107">*init* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83be2-108">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="83be2-108">Type: **BOOL**</span></span>

<span data-ttu-id="83be2-109">**Значение true** , чтобы зарегистрировать текущий процесс в качестве узла DDE; **Значение false** , чтобы отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="83be2-109">**TRUE** to register the current process as DDE host; **FALSE** to unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83be2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83be2-110">Return value</span></span>

<span data-ttu-id="83be2-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="83be2-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83be2-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="83be2-112">Remarks</span></span>

<span data-ttu-id="83be2-113">Процесс, вызывающий эту функцию, выступает в качестве оболочки и используется для просмотра содержимого папок, открытых с помощью команды "Open" [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="83be2-113">The process that calls this function acts as the Shell and is used to view the content of folders opened with the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 'open' verb.</span></span>

<span data-ttu-id="83be2-114">Эта функция не имеет связанного заголовка или файла библиотеки, поэтому она должна вызываться по порядковому значению.</span><span class="sxs-lookup"><span data-stu-id="83be2-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="83be2-115">Вызовите [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) с именем DLL (Shdocvw.dll), чтобы получить маркер модуля.</span><span class="sxs-lookup"><span data-stu-id="83be2-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Shdocvw.dll) to obtain a module handle.</span></span> <span data-ttu-id="83be2-116">Затем вызовите [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) с этим обработчиком модуля и номером функции с порядковым номером 118, чтобы получить адрес функции.</span><span class="sxs-lookup"><span data-stu-id="83be2-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the function ordinal number 118 to get the address of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="83be2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="83be2-117">Requirements</span></span>



| <span data-ttu-id="83be2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="83be2-118">Requirement</span></span> | <span data-ttu-id="83be2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="83be2-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83be2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83be2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83be2-121">Windows XP, \[ только для настольных приложений windows 2000 Professional\]</span><span class="sxs-lookup"><span data-stu-id="83be2-121">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="83be2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83be2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83be2-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="83be2-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="83be2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="83be2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83be2-125"><dt>Shdocvw.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="83be2-125"><dt>Shdocvw.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
