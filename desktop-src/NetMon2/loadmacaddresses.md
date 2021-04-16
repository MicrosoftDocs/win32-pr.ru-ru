---
description: Функция Лоадмакаддрессес вызывается монитором для заполнения списка MAC-адресов адресами, полученными из строковой переменной конфигурации HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: Функция Лоадмакаддрессес (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 62c9422469d7acf061578d1ec093676f6e1d8386
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542383"
---
# <a name="loadmacaddresses-function"></a><span data-ttu-id="fc12d-103">Функция Лоадмакаддрессес</span><span class="sxs-lookup"><span data-stu-id="fc12d-103">LoadMACAddresses function</span></span>

<span data-ttu-id="fc12d-104">Функция **лоадмакаддрессес** вызывается монитором для заполнения списка MAC-адресов адресами, полученными из строковой переменной конфигурации HTML.</span><span class="sxs-lookup"><span data-stu-id="fc12d-104">The **LoadMACAddresses** function is called by the monitor to fill in a MAC address list with addresses taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc12d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc12d-105">Syntax</span></span>


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="fc12d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc12d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc12d-107">*pConfig* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc12d-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc12d-108">Указатель на строку конфигурации HTML, переданную в монитор методом [имонитор::D оконфигуре](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="fc12d-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="fc12d-109">*пварнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fc12d-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc12d-110">Указатель на имя переменной в строке конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fc12d-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="fc12d-111">*ппаддрессес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fc12d-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc12d-112">Указатель на указатель на массив адресов.</span><span class="sxs-lookup"><span data-stu-id="fc12d-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="fc12d-113">Если переменная, указанная в *пварнаме* , найдена и имеет ненулевую длину, функция выделяет достаточно места (с помощью **хеапаллокмемори**) и сохраняет все Mac-адреса в виде массива.</span><span class="sxs-lookup"><span data-stu-id="fc12d-113">If the variable specified in *pVarName* is found and has a non-zero-length, the function allocates sufficient space (by using **HeapAllocMemory**) and stores all the MAC addresses as an array.</span></span>

</dd> <dt>

<span data-ttu-id="fc12d-114">*пнумаддрессес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="fc12d-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc12d-115">Указатель на переменную **DWORD** , для которой задано количество MAC-адресов, полученных из строки конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fc12d-115">Pointer to the **DWORD** variable that is set to the number of MAC addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc12d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fc12d-116">Return value</span></span>

<span data-ttu-id="fc12d-117">Если функция выполнена успешно, (имя переменной было обнаружено и имело строку ненулевой длины, представляющую MAC-адреса), возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="fc12d-117">If the function is successful, (the variable name was found and had a non-zero-length string that represented MAC addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="fc12d-118">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="fc12d-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc12d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="fc12d-119">Requirements</span></span>



| <span data-ttu-id="fc12d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="fc12d-120">Requirement</span></span> | <span data-ttu-id="fc12d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="fc12d-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fc12d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc12d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fc12d-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc12d-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="fc12d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc12d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fc12d-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fc12d-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="fc12d-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="fc12d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc12d-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc12d-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="fc12d-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fc12d-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc12d-129"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc12d-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="fc12d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fc12d-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc12d-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc12d-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




