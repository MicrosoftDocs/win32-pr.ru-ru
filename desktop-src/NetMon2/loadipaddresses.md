---
description: Функция Лоадипаддрессес вызывается монитором для заполнения списка IP-адресов адресами, полученными из строковой переменной конфигурации HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: Функция Лоадипаддрессес (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a5c172117081777b2a89b875401ec0645dd643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674481"
---
# <a name="loadipaddresses-function"></a><span data-ttu-id="daa9f-103">Функция Лоадипаддрессес</span><span class="sxs-lookup"><span data-stu-id="daa9f-103">LoadIPAddresses function</span></span>

<span data-ttu-id="daa9f-104">Функция **лоадипаддрессес** вызывается монитором для заполнения списка IP-адресов адресами, полученными из строковой переменной конфигурации HTML.</span><span class="sxs-lookup"><span data-stu-id="daa9f-104">The **LoadIPAddresses** function is called by the monitor to fill in an IP address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="daa9f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="daa9f-105">Syntax</span></span>


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="daa9f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="daa9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daa9f-107">*pConfig* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="daa9f-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daa9f-108">Указатель на строку конфигурации HTML, переданную в монитор методом [имонитор::D оконфигуре](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="daa9f-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="daa9f-109">*пварнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="daa9f-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daa9f-110">Указатель на имя переменной в строке конфигурации.</span><span class="sxs-lookup"><span data-stu-id="daa9f-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="daa9f-111">*ппаддрессес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="daa9f-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="daa9f-112">Указатель на указатель на массив адресов.</span><span class="sxs-lookup"><span data-stu-id="daa9f-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="daa9f-113">Если переменная, указанная в *пварнаме* , найдена и имеет ненулевую длину, функция выделяет достаточно места и сохраняет все IP-адреса в виде массива.</span><span class="sxs-lookup"><span data-stu-id="daa9f-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space and stores all the IP addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="daa9f-114">*пнумаддрессес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="daa9f-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="daa9f-115">Указатель на переменную **DWORD** , для которой задано количество IP-адресов, полученных из строки конфигурации.</span><span class="sxs-lookup"><span data-stu-id="daa9f-115">Pointer to the **DWORD** variable that is set to the number of IP addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daa9f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="daa9f-116">Return value</span></span>

<span data-ttu-id="daa9f-117">Если функция выполнена успешно (имя переменной было обнаружено и имело строку ненулевой длины, которая представляет IP-адреса), возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="daa9f-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IP addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="daa9f-118">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="daa9f-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="daa9f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="daa9f-119">Remarks</span></span>

<span data-ttu-id="daa9f-120">IP-адреса должны быть в формате x. x. x. x (например, 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="daa9f-120">The IP addresses must be in x.x.x.x format (for example, 127.0.0.1).</span></span>

## <a name="requirements"></a><span data-ttu-id="daa9f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="daa9f-121">Requirements</span></span>



| <span data-ttu-id="daa9f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="daa9f-122">Requirement</span></span> | <span data-ttu-id="daa9f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="daa9f-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="daa9f-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="daa9f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="daa9f-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="daa9f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="daa9f-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="daa9f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="daa9f-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="daa9f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="daa9f-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="daa9f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="daa9f-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="daa9f-129"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="daa9f-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="daa9f-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="daa9f-131"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="daa9f-131"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="daa9f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="daa9f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="daa9f-133"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daa9f-133"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




