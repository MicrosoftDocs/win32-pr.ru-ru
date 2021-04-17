---
description: Функция Аддпринтпровидор устанавливает локальный поставщик печати и связывает файлы конфигурации, данных и поставщика.
ms.assetid: f34549c3-0474-48ba-9307-5b36f02dbe1c
title: Функция Аддпринтпровидор (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProvidor
- AddPrintProvidorA
- AddPrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: adf5f914046eb82e070e3e9915325989ff868d1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673635"
---
# <a name="addprintprovidor-function"></a><span data-ttu-id="a5270-103">Функция Аддпринтпровидор</span><span class="sxs-lookup"><span data-stu-id="a5270-103">AddPrintProvidor function</span></span>

<span data-ttu-id="a5270-104">Функция **аддпринтпровидор** устанавливает локальный поставщик печати и связывает файлы конфигурации, данных и поставщика.</span><span class="sxs-lookup"><span data-stu-id="a5270-104">The **AddPrintProvidor** function installs a local print provider and links the configuration, data, and provider files.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5270-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5270-105">Syntax</span></span>


```C++
BOOL AddPrintProvidor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pProviderInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a5270-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a5270-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5270-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5270-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5270-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором должен быть установлен поставщик.</span><span class="sxs-lookup"><span data-stu-id="a5270-108">A pointer to a null-terminated string that specifies the name of the server on which the provider should be installed.</span></span> <span data-ttu-id="a5270-109">Для систем, которые поддерживают только локальную установку поставщиков, этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a5270-109">For systems that only support local installation of providers, this parameter should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a5270-110">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5270-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5270-111">Уровень структуры, на которую указывает *ппровидеринфо* .</span><span class="sxs-lookup"><span data-stu-id="a5270-111">The level of the structure to which *pProviderInfo* points.</span></span> <span data-ttu-id="a5270-112">Может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="a5270-112">It can be one of the following.</span></span>



| <span data-ttu-id="a5270-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a5270-113">Value</span></span>                                                                                                | <span data-ttu-id="a5270-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a5270-114">Meaning</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <span data-ttu-id="a5270-115"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a5270-115"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a5270-116">Функция использует структуру [**провидор \_ info \_ 1**](providor-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="a5270-116">Function uses a [**PROVIDOR\_INFO\_1**](providor-info-1.md) structure.</span></span><br/> |
| <span id="2"></span><dl> <span data-ttu-id="a5270-117"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a5270-117"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a5270-118">Функция использует структуру [**провидор \_ info \_ 2**](providor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="a5270-118">Function uses a [**PROVIDOR\_INFO\_2**](providor-info-2.md) structure.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a5270-119">*ппровидеринфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a5270-119">*pProviderInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5270-120">Указатель на структуру поставщика печати, как указано в *уровне*.</span><span class="sxs-lookup"><span data-stu-id="a5270-120">A pointer to a print provider structure, as indicated by *Level*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5270-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a5270-121">Return value</span></span>

<span data-ttu-id="a5270-122">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="a5270-122">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a5270-123">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="a5270-123">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5270-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5270-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a5270-125">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="a5270-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a5270-126">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="a5270-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a5270-127">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="a5270-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a5270-128">Прежде чем приложение вызовет функцию **аддпринтпровидор** , все файлы, необходимые поставщику, необходимо скопировать в каталог System32.</span><span class="sxs-lookup"><span data-stu-id="a5270-128">Before an application calls the **AddPrintProvidor** function, all files required by the provider must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="a5270-129">Поставщик, добавленный с помощью **аддпринтпровидор** , может быть удален путем вызова [**делетепринтпровидор**](deleteprintprovidor.md).</span><span class="sxs-lookup"><span data-stu-id="a5270-129">A provider added by **AddPrintProvidor** may be removed by calling [**DeletePrintProvidor**](deleteprintprovidor.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5270-130">Требования</span><span class="sxs-lookup"><span data-stu-id="a5270-130">Requirements</span></span>



| <span data-ttu-id="a5270-131">Требование</span><span class="sxs-lookup"><span data-stu-id="a5270-131">Requirement</span></span> | <span data-ttu-id="a5270-132">Значение</span><span class="sxs-lookup"><span data-stu-id="a5270-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5270-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a5270-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a5270-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5270-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a5270-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a5270-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a5270-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a5270-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a5270-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a5270-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5270-138"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5270-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a5270-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a5270-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5270-140"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5270-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a5270-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a5270-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5270-142"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a5270-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a5270-143">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="a5270-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a5270-144">**Аддпринтпровидорв** (Юникод) и **аддпринтпровидора** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a5270-144">**AddPrintProvidorW** (Unicode) and **AddPrintProvidorA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="a5270-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a5270-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5270-146">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="a5270-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a5270-147">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="a5270-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a5270-148">**делетепринтпровидор**</span><span class="sxs-lookup"><span data-stu-id="a5270-148">**DeletePrintProvidor**</span></span>](deleteprintprovidor.md)
</dt> <dt>

[<span data-ttu-id="a5270-149">**\_Сведения о провидор \_ 1**</span><span class="sxs-lookup"><span data-stu-id="a5270-149">**PROVIDOR\_INFO\_1**</span></span>](providor-info-1.md)
</dt> <dt>

[<span data-ttu-id="a5270-150">**\_Сведения о провидор \_ 2**</span><span class="sxs-lookup"><span data-stu-id="a5270-150">**PROVIDOR\_INFO\_2**</span></span>](providor-info-2.md)
</dt> </dl>

 

 




