---
description: Функция Лоаддворд вызывается монитором для задания переменной типа DWORD значения, взятого из строковой переменной конфигурации HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: Функция Лоаддворд (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1c66566090e38fc936a5616c8782284ad795df29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674363"
---
# <a name="loaddword-function"></a><span data-ttu-id="44dc8-103">Функция Лоаддворд</span><span class="sxs-lookup"><span data-stu-id="44dc8-103">LoadDWORD function</span></span>

<span data-ttu-id="44dc8-104">Функция **лоаддворд** вызывается монитором для задания переменной **типа DWORD** значения, взятого из строковой переменной конфигурации HTML.</span><span class="sxs-lookup"><span data-stu-id="44dc8-104">The **LoadDWORD** function is called by the monitor to set a **DWORD** variable with a value taken from an HTML configuration string variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="44dc8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44dc8-105">Syntax</span></span>


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="44dc8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="44dc8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44dc8-107">*pConfig* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44dc8-107">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44dc8-108">Указатель на строку конфигурации HTML, переданную в монитор методом [имонитор::D оконфигуре](imonitor-doconfigure.md) .</span><span class="sxs-lookup"><span data-stu-id="44dc8-108">Pointer to the HTML configuration string passed to the monitor by the [IMonitor::DoConfigure](imonitor-doconfigure.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="44dc8-109">*пварнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44dc8-109">*pVarName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44dc8-110">Указатель на имя переменной в строке конфигурации.</span><span class="sxs-lookup"><span data-stu-id="44dc8-110">Pointer to the name of the variable in the configuration string.</span></span>

</dd> <dt>

<span data-ttu-id="44dc8-111">*pValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="44dc8-111">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44dc8-112">Указатель на переменную **DWORD** , для которой задано значение переменной строки конфигурации.</span><span class="sxs-lookup"><span data-stu-id="44dc8-112">Pointer to the **DWORD** variable that is set to the value of the configuration string variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44dc8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44dc8-113">Return value</span></span>

<span data-ttu-id="44dc8-114">Если функция выполнена успешно (если имя переменной было обнаружено и имело строку, отличную от нулевой длины), то вставляется **параметр DWORD** , а возвращаемое значение — **true**.</span><span class="sxs-lookup"><span data-stu-id="44dc8-114">If the function is successful (if the variable name was found and had a non-zero-length string), the **DWORD** is inserted, and the return value is **TRUE**.</span></span>

<span data-ttu-id="44dc8-115">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="44dc8-115">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="44dc8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="44dc8-116">Requirements</span></span>



| <span data-ttu-id="44dc8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="44dc8-117">Requirement</span></span> | <span data-ttu-id="44dc8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="44dc8-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44dc8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44dc8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="44dc8-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44dc8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="44dc8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44dc8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="44dc8-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44dc8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="44dc8-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="44dc8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="44dc8-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="44dc8-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="44dc8-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44dc8-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="44dc8-126"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44dc8-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="44dc8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="44dc8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44dc8-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44dc8-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




