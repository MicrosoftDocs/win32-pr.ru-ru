---
description: Функция Буилдинипас возвращает полный путь к INI-файлу, который соответствует введенным данным.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Функция Буилдинипас (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663649"
---
# <a name="buildinipath-function"></a><span data-ttu-id="424e3-103">Функция Буилдинипас</span><span class="sxs-lookup"><span data-stu-id="424e3-103">BuildINIPath function</span></span>

<span data-ttu-id="424e3-104">Функция **буилдинипас** возвращает полный путь к INI-файлу, который соответствует введенным данным.</span><span class="sxs-lookup"><span data-stu-id="424e3-104">The **BuildINIPath** function returns a fully qualified path to an INI file that corresponds to information you enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="424e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="424e3-105">Syntax</span></span>


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a><span data-ttu-id="424e3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="424e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="424e3-107">*FullPath*</span><span class="sxs-lookup"><span data-stu-id="424e3-107">*FullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="424e3-108">Буфер, который получает полное имя INI-файла.</span><span class="sxs-lookup"><span data-stu-id="424e3-108">Buffer that receives the fully qualified INI file name.</span></span>

</dd> <dt>

<span data-ttu-id="424e3-109">*инифиленаме*</span><span class="sxs-lookup"><span data-stu-id="424e3-109">*IniFileName*</span></span> 
</dt> <dd>

<span data-ttu-id="424e3-110">Имя INI-файла (полное имя файла минус расширение имени файла).</span><span class="sxs-lookup"><span data-stu-id="424e3-110">Name of the INI file (the full file name minus the filename extension).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="424e3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="424e3-111">Return value</span></span>

<span data-ttu-id="424e3-112">Если функция выполнена успешно, возвращаемое значение является указателем на полное имя INI-файла.</span><span class="sxs-lookup"><span data-stu-id="424e3-112">If the function is successful, the return value is a pointer to the fully qualified INI file name.</span></span>

<span data-ttu-id="424e3-113">Если функция завершилась неудачно, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="424e3-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="424e3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="424e3-114">Remarks</span></span>

<span data-ttu-id="424e3-115">Путь, возвращаемый этой функцией, является полным путем к INI-файлу, который соответствует введенным данным.</span><span class="sxs-lookup"><span data-stu-id="424e3-115">The path that this function returns is a fully qualified path to an INI file that corresponds to information you enter.</span></span> <span data-ttu-id="424e3-116">Например, если ввести КСНС или TCP, функция создает путь к Xns.ini или Tcp.ini соответственно.</span><span class="sxs-lookup"><span data-stu-id="424e3-116">For example, if you enter XNS or TCP, the function generates a path to Xns.ini or Tcp.ini, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="424e3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="424e3-117">Requirements</span></span>



| <span data-ttu-id="424e3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="424e3-118">Requirement</span></span> | <span data-ttu-id="424e3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="424e3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="424e3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="424e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="424e3-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="424e3-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="424e3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="424e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="424e3-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="424e3-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="424e3-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="424e3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="424e3-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="424e3-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="424e3-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="424e3-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="424e3-127"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="424e3-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="424e3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="424e3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="424e3-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="424e3-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




