---
description: Функция Лоадтчар вызывается мониторами для задания строковой переменной строки, взятой из строки конфигурации HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: Функция Лоадтчар (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673319"
---
# <a name="loadtchar-function"></a><span data-ttu-id="156fd-103">Функция Лоадтчар</span><span class="sxs-lookup"><span data-stu-id="156fd-103">LoadTCHAR function</span></span>

<span data-ttu-id="156fd-104">Функция **лоадтчар** вызывается мониторами для задания строковой переменной строки, взятой из строки конфигурации HTML.</span><span class="sxs-lookup"><span data-stu-id="156fd-104">The **LoadTCHAR** function is called by monitors to set a string variable to a string taken from an HTML configuration string.</span></span>

## <a name="syntax"></a><span data-ttu-id="156fd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="156fd-105">Syntax</span></span>


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
);
```



## <a name="parameters"></a><span data-ttu-id="156fd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="156fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="156fd-107">*pConfig* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="156fd-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="156fd-108">Указатель на строку конфигурации HTML, переданную в монитор методом [имонитор::D оконфигуре](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="156fd-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="156fd-109">*пварнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="156fd-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="156fd-110">Указатель на имя переменной в строке конфигурации.</span><span class="sxs-lookup"><span data-stu-id="156fd-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="156fd-111">*ппсзстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="156fd-111">*ppszString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="156fd-112">Указатель на указатель строки.</span><span class="sxs-lookup"><span data-stu-id="156fd-112">Pointer to a string pointer.</span></span> <span data-ttu-id="156fd-113">Если запрошенное имя переменной найдено, строка выделяется и присваивается этому указателю.</span><span class="sxs-lookup"><span data-stu-id="156fd-113">If the requested variable name is found, the string is allocated and assigned to this pointer.</span></span> <span data-ttu-id="156fd-114">Это пользователь, ответственный за освобождение памяти, связанной со строкой.</span><span class="sxs-lookup"><span data-stu-id="156fd-114">It is the user's responsibly to free the memory associated with the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="156fd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="156fd-115">Return value</span></span>

<span data-ttu-id="156fd-116">Если функция выполнена успешно (если имя переменной было обнаружено и имело строку ненулевой длины), возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="156fd-116">If the function is successful (if the variable name was found and had a non-zero-length string), the return value is **TRUE**.</span></span>

<span data-ttu-id="156fd-117">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="156fd-117">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="156fd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="156fd-118">Requirements</span></span>



| <span data-ttu-id="156fd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="156fd-119">Requirement</span></span> | <span data-ttu-id="156fd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="156fd-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="156fd-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="156fd-121">Minimum supported client</span></span><br/> | <span data-ttu-id="156fd-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="156fd-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="156fd-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="156fd-123">Minimum supported server</span></span><br/> | <span data-ttu-id="156fd-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="156fd-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="156fd-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="156fd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="156fd-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="156fd-126"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="156fd-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="156fd-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="156fd-128"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="156fd-128"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="156fd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="156fd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="156fd-130"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="156fd-130"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




