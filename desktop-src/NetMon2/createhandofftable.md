---
description: Функция Креатехандоффтабле создает таблицу передачи, которая включает сведения о передаче данных, хранящихся в INI-файле средства синтаксического анализа.
ms.assetid: 6dbca2fa-33fb-48e8-b663-be59aec6264b
title: Функция Креатехандоффтабле (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 450bb4e4b158a937d48d753a5ff5c831f8fa58c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663025"
---
# <a name="createhandofftable-function"></a><span data-ttu-id="c7adc-103">Функция Креатехандоффтабле</span><span class="sxs-lookup"><span data-stu-id="c7adc-103">CreateHandoffTable function</span></span>

<span data-ttu-id="c7adc-104">Функция **креатехандоффтабле** создает [*таблицу*](h.md) передачи, которая включает сведения о передаче данных, хранящихся в ini-файле средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="c7adc-104">The **CreateHandoffTable** function creates a [*handoff table*](h.md) that includes the handoff set information stored in the INI file of the parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7adc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7adc-105">Syntax</span></span>


```C++
DWORD WINAPI CreateHandoffTable(
  _In_  LPSTR          secName,
  _In_  LPSTR          iniFile,
  _Out_ LPHANDOFFTABLE *hTable,
  _In_  DWORD          nMaxProtocolEntries,
  _In_  DWORD          base
);
```



## <a name="parameters"></a><span data-ttu-id="c7adc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7adc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7adc-107">*секнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7adc-107">*secName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7adc-108">Строка, указывающая раздел INI-файла, в котором находятся сведения о переданном наборе.</span><span class="sxs-lookup"><span data-stu-id="c7adc-108">String that indicates the section of the INI file where the handoff set information is located.</span></span>

</dd> <dt>

<span data-ttu-id="c7adc-109">*инифиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7adc-109">*iniFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7adc-110">Строка, содержащая имя INI-файла средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="c7adc-110">String that includes the name of the parser INI file.</span></span>

</dd> <dt>

<span data-ttu-id="c7adc-111">*хтабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c7adc-111">*hTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7adc-112">Обработчик для структуры **хандоффтабле** , созданной и обслуживаемой сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="c7adc-112">Handle to a **HANDOFFTABLE** structure created and maintained by Network Monitor.</span></span>

</dd> <dt>

<span data-ttu-id="c7adc-113">*нмакспротоколентриес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7adc-113">*nMaxProtocolEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7adc-114">Число, указывающее максимальное число записей, которое может обработать переданная таблица.</span><span class="sxs-lookup"><span data-stu-id="c7adc-114">Number that specifies the maximum number of entries that the handoff table can process.</span></span>

</dd> <dt>

<span data-ttu-id="c7adc-115">*базовый* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7adc-115">*base* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7adc-116">Числовой набор номеров переданных наборов, хранящихся в INI-файле.</span><span class="sxs-lookup"><span data-stu-id="c7adc-116">Numerical base of handoff set numbers stored in the INI file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7adc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7adc-117">Return value</span></span>

<span data-ttu-id="c7adc-118">Если функция выполнена успешно, возвращаемое значение равно количеству записей в таблице передачи.</span><span class="sxs-lookup"><span data-stu-id="c7adc-118">If the function is successful, the return value is the number of entries in the handoff table.</span></span>

<span data-ttu-id="c7adc-119">Если функция завершилась неудачно, возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c7adc-119">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7adc-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7adc-120">Remarks</span></span>

<span data-ttu-id="c7adc-121">Таблица передачи, созданная сетевой монитор, основана на сведениях, предоставленных в INI-файле средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="c7adc-121">The handoff table created by Network Monitor is based on information provided in the parser INI.</span></span> <span data-ttu-id="c7adc-122">Возвращаемый обработчик для переданной таблицы может использоваться для получения маркера для одного из протоколов, входящих в таблицу.</span><span class="sxs-lookup"><span data-stu-id="c7adc-122">The returned handle to the handoff table can then be used to obtain a handle to one of the protocols included in the table.</span></span> <span data-ttu-id="c7adc-123">Чтобы получить маркер одного из этих протоколов, вызовите [жетпротоколфромтабле](getprotocolfromtable.md).</span><span class="sxs-lookup"><span data-stu-id="c7adc-123">To obtain a handle of one of these protocols, call [GetProtocolFromTable](getprotocolfromtable.md).</span></span>

<span data-ttu-id="c7adc-124">Обратите внимание, что приложение синтаксического анализа никогда не обращается к структуре **хандоффтабле** напрямую.</span><span class="sxs-lookup"><span data-stu-id="c7adc-124">Notice that the parser application never accesses the **HANDOFFTABLE** structure directly.</span></span> <span data-ttu-id="c7adc-125">Эта структура создается и обслуживается сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="c7adc-125">This structure is created and maintained by Network Monitor.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7adc-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c7adc-126">Requirements</span></span>



| <span data-ttu-id="c7adc-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c7adc-127">Requirement</span></span> | <span data-ttu-id="c7adc-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c7adc-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c7adc-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7adc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c7adc-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c7adc-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="c7adc-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7adc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c7adc-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c7adc-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c7adc-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c7adc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7adc-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7adc-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c7adc-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c7adc-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7adc-136"><dt>Нмапи. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7adc-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="c7adc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c7adc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7adc-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7adc-138"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7adc-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7adc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7adc-140">жетпротоколфромтабле</span><span class="sxs-lookup"><span data-stu-id="c7adc-140">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> <dt>

[<span data-ttu-id="c7adc-141">хандоффтабле</span><span class="sxs-lookup"><span data-stu-id="c7adc-141">HANDOFFTABLE</span></span>](handofftable.md)
</dt> </dl>

 

 




