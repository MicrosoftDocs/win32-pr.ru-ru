---
description: Функция Лоадипксаддрессес вызывается монитором для заполнения списка IPX-адресов, взятого из строковой переменной конфигурации HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: Функция Лоадипксаддрессес (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f6e25e7afa80c3a3c4113723937c623baacd2a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272062"
---
# <a name="loadipxaddresses-function"></a><span data-ttu-id="67499-103">Функция Лоадипксаддрессес</span><span class="sxs-lookup"><span data-stu-id="67499-103">LoadIPXAddresses function</span></span>

<span data-ttu-id="67499-104">Функция **лоадипксаддрессес** вызывается монитором для заполнения списка IPX-адресов, взятого из строковой переменной конфигурации HTML.</span><span class="sxs-lookup"><span data-stu-id="67499-104">The **LoadIPXAddresses** function is called by the monitor to fill in an IPX address list taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="67499-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67499-105">Syntax</span></span>


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="67499-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="67499-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67499-107">*pConfig* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67499-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67499-108">Указатель на строку конфигурации HTML, переданную в монитор методом [имонитор::D оконфигуре](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="67499-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="67499-109">*пварнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67499-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67499-110">Указатель на имя переменной в строке конфигурации.</span><span class="sxs-lookup"><span data-stu-id="67499-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="67499-111">*ппаддрессес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="67499-111">*ppAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67499-112">Указатель на указатель на массив адресов.</span><span class="sxs-lookup"><span data-stu-id="67499-112">Pointer to a pointer to an array of addresses.</span></span> <span data-ttu-id="67499-113">Если переменная, указанная в *пварнаме* , найдена и имеет ненулевую длину, выделяется достаточно места (с помощью **хеапаллокмемори**), а все IPX-адреса хранятся в виде массива.</span><span class="sxs-lookup"><span data-stu-id="67499-113">If the variable specified in *pVarName* is found and has a non-zero-length, sufficient space is allocated (by using **HeapAllocMemory**), and all the IPX addresses are stored as an array.</span></span>

</dd> <dt>

<span data-ttu-id="67499-114">*пнумаддрессес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="67499-114">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67499-115">Указатель на переменную **DWORD** , для которой задано количество IPX-адресов, полученных из строки конфигурации.</span><span class="sxs-lookup"><span data-stu-id="67499-115">Pointer to the **DWORD** variable that is set to the number of IPX addresses taken from the configuration string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67499-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67499-116">Return value</span></span>

<span data-ttu-id="67499-117">Если функция выполнена успешно (обнаружено имя переменной, имеющее строку, отличную от нулевой длины, которая представляет IPX-адреса), возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="67499-117">If the function is successful (the variable name was found and had a non-zero-length string that represented IPX addresses), the return value is **TRUE**.</span></span>

<span data-ttu-id="67499-118">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="67499-118">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="67499-119">Требования</span><span class="sxs-lookup"><span data-stu-id="67499-119">Requirements</span></span>



| <span data-ttu-id="67499-120">Требование</span><span class="sxs-lookup"><span data-stu-id="67499-120">Requirement</span></span> | <span data-ttu-id="67499-121">Значение</span><span class="sxs-lookup"><span data-stu-id="67499-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="67499-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="67499-122">Minimum supported client</span></span><br/> | <span data-ttu-id="67499-123">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="67499-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="67499-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="67499-124">Minimum supported server</span></span><br/> | <span data-ttu-id="67499-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="67499-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="67499-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="67499-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="67499-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="67499-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="67499-128">Библиотека</span><span class="sxs-lookup"><span data-stu-id="67499-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="67499-129"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67499-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="67499-130">DLL</span><span class="sxs-lookup"><span data-stu-id="67499-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67499-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67499-131"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




