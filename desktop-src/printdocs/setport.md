---
description: Функция Сетпорт задает состояние, связанное с портом принтера.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: Функция Сетпорт (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080740"
---
# <a name="setport-function"></a><span data-ttu-id="292b6-103">Функция Сетпорт</span><span class="sxs-lookup"><span data-stu-id="292b6-103">SetPort function</span></span>

<span data-ttu-id="292b6-104">Функция **сетпорт** задает состояние, связанное с портом принтера.</span><span class="sxs-lookup"><span data-stu-id="292b6-104">The **SetPort** function sets the status associated with a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="292b6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="292b6-105">Syntax</span></span>


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a><span data-ttu-id="292b6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="292b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="292b6-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="292b6-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="292b6-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера печати, к которому подключен порт.</span><span class="sxs-lookup"><span data-stu-id="292b6-108">Pointer to a zero-terminated string that specifies the name of the printer server to which the port is connected.</span></span> <span data-ttu-id="292b6-109">Присвойте этому параметру **значение NULL** , если порт находится на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="292b6-109">Set this parameter to **NULL** if the port is on the local machine.</span></span>

</dd> <dt>

<span data-ttu-id="292b6-110">*ппортнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="292b6-110">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="292b6-111">Указатель на строку, завершающуюся нулем, которая указывает имя порта принтера.</span><span class="sxs-lookup"><span data-stu-id="292b6-111">Pointer to a zero-terminated string that specifies the name of the printer port.</span></span>

</dd> <dt>

<span data-ttu-id="292b6-112">*двлевел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="292b6-112">*dwLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="292b6-113">Указывает тип структуры, на которую указывает параметр *ппортинфо* .</span><span class="sxs-lookup"><span data-stu-id="292b6-113">Specifies the type of structure pointed to by the *pPortInfo* parameter.</span></span>

<span data-ttu-id="292b6-114">Это значение должно быть равно 3, что соответствует структуре [**данных \_ порта \_ 3**](port-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="292b6-114">This value must be 3, which corresponds to a [**PORT\_INFO\_3**](port-info-3.md) data structure.</span></span>

</dd> <dt>

<span data-ttu-id="292b6-115">*ппортинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="292b6-115">*pPortInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="292b6-116">Указатель на структуру с [**портом \_ \_ 3**](port-info-3.md) , содержащую сведения о состоянии порта, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="292b6-116">Pointer to a [**PORT\_INFO\_3**](port-info-3.md) structure that contains the port status information to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="292b6-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="292b6-117">Return value</span></span>

<span data-ttu-id="292b6-118">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="292b6-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="292b6-119">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="292b6-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="292b6-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="292b6-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="292b6-121">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="292b6-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="292b6-122">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="292b6-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="292b6-123">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="292b6-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="292b6-124">Вызывающая функция **сетпорт** должна выполняться от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="292b6-124">The caller of the **SetPort** function must be executing as an Administrator.</span></span> <span data-ttu-id="292b6-125">Кроме того, если вызывающий объект является монитором порта или монитором языка, он должен вызвать [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) для прекращения олицетворения перед вызовом **сетпорт**.</span><span class="sxs-lookup"><span data-stu-id="292b6-125">Additionally, if the caller is a Port Monitor or Language Monitor, it must call [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) to cease impersonation before it calls **SetPort**.</span></span>

<span data-ttu-id="292b6-126">Все программы, вызывающие **сетпорт** , должны иметь доступ к серверу для \_ \_ администрирования доступа к серверу, к которому подключен порт.</span><span class="sxs-lookup"><span data-stu-id="292b6-126">All programs that call **SetPort** must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="292b6-127">Если для параметра состояние порта принтера задано значение \_ \_ Ошибка тип состояния порта \_ , диспетчер очереди печати прекращает отправку заданий на порт.</span><span class="sxs-lookup"><span data-stu-id="292b6-127">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="292b6-128">Диспетчер очереди печати возобновляет отправку заданий в порт, когда состояние порта сбрасывается другим вызовом **сетпорт**.</span><span class="sxs-lookup"><span data-stu-id="292b6-128">The print spooler resumes sending jobs to the port when the port status is cleared by another call to **SetPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="292b6-129">Требования</span><span class="sxs-lookup"><span data-stu-id="292b6-129">Requirements</span></span>



| <span data-ttu-id="292b6-130">Требование</span><span class="sxs-lookup"><span data-stu-id="292b6-130">Requirement</span></span> | <span data-ttu-id="292b6-131">Значение</span><span class="sxs-lookup"><span data-stu-id="292b6-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="292b6-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="292b6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="292b6-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="292b6-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="292b6-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="292b6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="292b6-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="292b6-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="292b6-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="292b6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="292b6-137"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="292b6-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="292b6-138">Библиотека</span><span class="sxs-lookup"><span data-stu-id="292b6-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="292b6-139"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="292b6-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="292b6-140">DLL</span><span class="sxs-lookup"><span data-stu-id="292b6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="292b6-141"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="292b6-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="292b6-142">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="292b6-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="292b6-143">**Сетпортв** (Юникод) и **сетпорта** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="292b6-143">**SetPortW** (Unicode) and **SetPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="292b6-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="292b6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="292b6-145">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="292b6-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="292b6-146">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="292b6-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="292b6-147">**\_Сведения о порте \_ 3**</span><span class="sxs-lookup"><span data-stu-id="292b6-147">**PORT\_INFO\_3**</span></span>](port-info-3.md)
</dt> </dl>

 

