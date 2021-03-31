---
description: Функция Адванцеддокументпропертиес отображает диалоговое окно настройки принтера для указанного принтера, позволяя пользователю настроить этот принтер.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: Функция Адванцеддокументпропертиес (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817769"
---
# <a name="advanceddocumentproperties-function"></a><span data-ttu-id="8915a-103">Функция Адванцеддокументпропертиес</span><span class="sxs-lookup"><span data-stu-id="8915a-103">AdvancedDocumentProperties function</span></span>

<span data-ttu-id="8915a-104">Функция **адванцеддокументпропертиес** отображает диалоговое окно настройки принтера для указанного принтера, позволяя пользователю настроить этот принтер.</span><span class="sxs-lookup"><span data-stu-id="8915a-104">The **AdvancedDocumentProperties** function displays a printer-configuration dialog box for the specified printer, allowing the user to configure that printer.</span></span>

<span data-ttu-id="8915a-105">Эта функция является особым случаем функции [**DocumentProperties**](documentproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="8915a-105">This function is a special case of the [**DocumentProperties**](documentproperties.md) function.</span></span> <span data-ttu-id="8915a-106">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="8915a-106">For more details, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="8915a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8915a-107">Syntax</span></span>


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a><span data-ttu-id="8915a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8915a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8915a-109">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8915a-109">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8915a-110">Маркер родительского окна диалогового окна настройки принтера.</span><span class="sxs-lookup"><span data-stu-id="8915a-110">A handle to the parent window of the printer-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="8915a-111">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8915a-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8915a-112">Маркер объекта принтера.</span><span class="sxs-lookup"><span data-stu-id="8915a-112">A handle to a printer object.</span></span> <span data-ttu-id="8915a-113">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="8915a-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="8915a-114">*пдевиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8915a-114">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8915a-115">Указатель на строку с завершающим нулем, указывающую имя устройства, для которого должно отображаться диалоговое окно настройки принтера.</span><span class="sxs-lookup"><span data-stu-id="8915a-115">A pointer to a null-terminated string specifying the name of the device for which a printer-configuration dialog box should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="8915a-116">*пдевмодеаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8915a-116">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8915a-117">Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , которая будет содержать данные конфигурации, указанные пользователем.</span><span class="sxs-lookup"><span data-stu-id="8915a-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that will contain the configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="8915a-118">*пдевмодеинпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8915a-118">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8915a-119">Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , содержащую данные конфигурации, используемые для инициализации элементов управления диалогового окна настройки принтера.</span><span class="sxs-lookup"><span data-stu-id="8915a-119">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains the configuration data used to initialize the controls of the printer-configuration dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8915a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8915a-120">Return value</span></span>

<span data-ttu-id="8915a-121">Если функция [**DocumentProperties**](documentproperties.md) с этими параметрами выполнена успешно, возвращаемое значение **адванцеддокументпропертиес** равно 1.</span><span class="sxs-lookup"><span data-stu-id="8915a-121">If the [**DocumentProperties**](documentproperties.md) function with these parameters is successful, the return value of **AdvancedDocumentProperties** is 1.</span></span> <span data-ttu-id="8915a-122">В противном случае возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="8915a-122">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="8915a-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8915a-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8915a-124">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="8915a-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8915a-125">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="8915a-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8915a-126">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="8915a-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8915a-127">Эта функция может отображать диалоговое окно Настройка принтера только для того, чтобы пользователь мог его настроить.</span><span class="sxs-lookup"><span data-stu-id="8915a-127">This function can only display the printer-configuration dialog box so a user can configure it.</span></span> <span data-ttu-id="8915a-128">Для получения дополнительных элементов управления используйте [**DocumentProperties**](documentproperties.md).</span><span class="sxs-lookup"><span data-stu-id="8915a-128">For more control, use [**DocumentProperties**](documentproperties.md).</span></span> <span data-ttu-id="8915a-129">Входные параметры для этой функции передаются непосредственно в **DocumentProperties** , а значение *фмоде* — DM \_ в \_ буфере \| DM \_ в \_ запросе \| DM \_ out \_ .</span><span class="sxs-lookup"><span data-stu-id="8915a-129">The input parameters for this function are passed directly to **DocumentProperties** and the *fMode* value is set to DM\_IN\_BUFFER \| DM\_IN\_PROMPT \| DM\_OUT\_BUFFER.</span></span> <span data-ttu-id="8915a-130">В отличие от **DocumentProperties**, эта функция возвращает только 1 или 0.</span><span class="sxs-lookup"><span data-stu-id="8915a-130">Unlike **DocumentProperties**, this function only returns 1 or 0.</span></span> <span data-ttu-id="8915a-131">Поэтому невозможно определить требуемый размер [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , установив для *пдевмоде* значение 0.</span><span class="sxs-lookup"><span data-stu-id="8915a-131">Thus, you cannot determine the required size of [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) by setting *pDevMode* to zero.</span></span>

<span data-ttu-id="8915a-132">Приложение может получить имя, на которое указывает параметр *пдевиценаме* , вызвав функцию « [**PrintOut**](getprinter.md) », а затем проверив элемент **ппринтернаме** в структуре « [**\_ сведения о принтере \_ 2**](printer-info-2.md) ».</span><span class="sxs-lookup"><span data-stu-id="8915a-132">An application can obtain the name pointed to by the *pDeviceName* parameter by calling the [**GetPrinter**](getprinter.md) function and then examining the **pPrinterName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="8915a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="8915a-133">Requirements</span></span>



| <span data-ttu-id="8915a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="8915a-134">Requirement</span></span> | <span data-ttu-id="8915a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8915a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8915a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8915a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8915a-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8915a-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8915a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8915a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8915a-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8915a-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8915a-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8915a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8915a-141"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8915a-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8915a-142">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8915a-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="8915a-143"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8915a-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8915a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8915a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8915a-145"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8915a-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8915a-146">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8915a-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8915a-147">**Адванцеддокументпропертиесв** (Юникод) и **адванцеддокументпропертиеса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8915a-147">**AdvancedDocumentPropertiesW** (Unicode) and **AdvancedDocumentPropertiesA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="8915a-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8915a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8915a-149">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="8915a-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8915a-150">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="8915a-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8915a-151">**аддпринтер**</span><span class="sxs-lookup"><span data-stu-id="8915a-151">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="8915a-152">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="8915a-152">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="8915a-153">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="8915a-153">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="8915a-154">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="8915a-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="8915a-155">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="8915a-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="8915a-156">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8915a-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




