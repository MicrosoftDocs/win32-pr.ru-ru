---
description: Функция DocumentProperties извлекает или изменяет сведения об инициализации принтера или отображает страницу свойств конфигурации принтера для указанного принтера.
ms.assetid: e89a2f6f-2bac-4369-b526-f8e15028698b
title: Функция DocumentProperties (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DocumentProperties
- DocumentPropertiesA
- DocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 732cb6901b444117d0599a2899327ebcb749cf74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156755"
---
# <a name="documentproperties-function"></a><span data-ttu-id="57cfd-103">Функция DocumentProperties</span><span class="sxs-lookup"><span data-stu-id="57cfd-103">DocumentProperties function</span></span>

<span data-ttu-id="57cfd-104">Функция **DocumentProperties** извлекает или изменяет сведения об инициализации принтера или отображает страницу свойств конфигурации принтера для указанного принтера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-104">The **DocumentProperties** function retrieves or modifies printer initialization information or displays a printer-configuration property sheet for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="57cfd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57cfd-105">Syntax</span></span>


```C++
LONG DocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput,
  _In_  DWORD    fMode
);
```



## <a name="parameters"></a><span data-ttu-id="57cfd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57cfd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57cfd-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57cfd-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cfd-108">Маркер родительского окна страницы свойств конфигурации принтера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-108">A handle to the parent window of the printer-configuration property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="57cfd-109">*хпринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57cfd-109">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cfd-110">Маркер объекта принтера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-110">A handle to a printer object.</span></span> <span data-ttu-id="57cfd-111">Используйте функцию [**опенпринтер**](openprinter.md) или [**аддпринтер**](addprinter.md) для получения маркера принтера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-111">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="57cfd-112">*пдевиценаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57cfd-112">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cfd-113">Указатель на строку, завершающуюся нулем, которая указывает имя устройства, для которого отображается страница свойств конфигурации принтера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-113">A pointer to a null-terminated string that specifies the name of the device for which the printer-configuration property sheet is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="57cfd-114">*пдевмодеаутпут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="57cfd-114">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57cfd-115">Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , которая получает данные конфигурации принтера, указанные пользователем.</span><span class="sxs-lookup"><span data-stu-id="57cfd-115">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that receives the printer configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="57cfd-116">*пдевмодеинпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57cfd-116">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cfd-117">Указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , которую операционная система использует для инициализации элементов управления страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="57cfd-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that the operating system uses to initialize the property sheet controls.</span></span>

<span data-ttu-id="57cfd-118">Этот параметр используется только в том случае, если флаг **DM \_ в \_ буфере** установлен в параметре *фмоде* .</span><span class="sxs-lookup"><span data-stu-id="57cfd-118">This parameter is only used if the **DM\_IN\_BUFFER** flag is set in the *fMode* parameter.</span></span> <span data-ttu-id="57cfd-119">Если **DM \_ в \_ буфере** не задан, операционная система использует для принтера [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="57cfd-119">If **DM\_IN\_BUFFER** is not set, the operating system uses the printer's default [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea).</span></span>

</dd> <dt>

<span data-ttu-id="57cfd-120">*фмоде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57cfd-120">*fMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57cfd-121">Операции, выполняемые функцией.</span><span class="sxs-lookup"><span data-stu-id="57cfd-121">The operations the function performs.</span></span> <span data-ttu-id="57cfd-122">Если этот параметр равен нулю, функция **DocumentProperties** возвращает число байтов, необходимых структуре данных [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-122">If this parameter is zero, the **DocumentProperties** function returns the number of bytes required by the printer driver's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure.</span></span> <span data-ttu-id="57cfd-123">В противном случае используйте одну или несколько из следующих констант для создания значения для этого параметра. Однако обратите внимание, что для изменения параметров печати приложение должно указать по крайней мере одно входное значение и одно выходное значение.</span><span class="sxs-lookup"><span data-stu-id="57cfd-123">Otherwise, use one or more of the following constants to construct a value for this parameter; note, however, that in order to change the print settings, an application must specify at least one input value and one output value.</span></span>



| <span data-ttu-id="57cfd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="57cfd-124">Value</span></span>                                                                                                                                                          | <span data-ttu-id="57cfd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="57cfd-125">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DM_IN_BUFFER"></span><span id="dm_in_buffer"></span><dl> <span data-ttu-id="57cfd-126"><dt>**DM \_ в \_ буфере**</dt></span><span class="sxs-lookup"><span data-stu-id="57cfd-126"><dt>**DM\_IN\_BUFFER**</dt></span></span> </dl>    | <span data-ttu-id="57cfd-127">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="57cfd-127">Input value.</span></span> <span data-ttu-id="57cfd-128">Перед запросом, копированием или обновлением функция объединяет текущие параметры печати драйвера принтера с параметрами в структуре [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , заданной параметром *пдевмодеинпут* .</span><span class="sxs-lookup"><span data-stu-id="57cfd-128">Before prompting, copying, or updating, the function merges the printer driver's current print settings with the settings in the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure specified by the *pDevModeInput* parameter.</span></span> <span data-ttu-id="57cfd-129">Функция обновляет структуру только для тех элементов, которые указаны в элементе **дмфиелдс** структуры **DEVMODE** .</span><span class="sxs-lookup"><span data-stu-id="57cfd-129">The function updates the structure only for those members specified by the **DEVMODE** structure's **dmFields** member.</span></span> <span data-ttu-id="57cfd-130">Это значение также определяется как **DM \_ Modify**.</span><span class="sxs-lookup"><span data-stu-id="57cfd-130">This value is also defined as **DM\_MODIFY**.</span></span> <span data-ttu-id="57cfd-131">В случае конфликта во время слияния параметры в структуре **DEVMODE** , заданной параметром *пдевмодеинпут* , переопределяют текущие параметры печати драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-131">In cases of conflict during the merge, the settings in the **DEVMODE** structure specified by *pDevModeInput* override the printer driver's current print settings.</span></span><br/> |
| <span id="DM_IN_PROMPT"></span><span id="dm_in_prompt"></span><dl> <span data-ttu-id="57cfd-132"><dt>**DM \_ в \_ запросе**</dt></span><span class="sxs-lookup"><span data-stu-id="57cfd-132"><dt>**DM\_IN\_PROMPT**</dt></span></span> </dl>    | <span data-ttu-id="57cfd-133">Входное значение.</span><span class="sxs-lookup"><span data-stu-id="57cfd-133">Input value.</span></span> <span data-ttu-id="57cfd-134">Функция представляет страницу свойств настройки печати драйвера принтера, а затем изменяет параметры структуры данных [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) принтера на значения, указанные пользователем.</span><span class="sxs-lookup"><span data-stu-id="57cfd-134">The function presents the printer driver's Print Setup property sheet and then changes the settings in the printer's [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure to those values specified by the user.</span></span> <span data-ttu-id="57cfd-135">Это значение также определяется как **\_ строка DM**.</span><span class="sxs-lookup"><span data-stu-id="57cfd-135">This value is also defined as **DM\_PROMPT**.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="DM_OUT_BUFFER"></span><span id="dm_out_buffer"></span><dl> <span data-ttu-id="57cfd-136"><dt>**\_выходной \_ буфер DM**</dt></span><span class="sxs-lookup"><span data-stu-id="57cfd-136"><dt>**DM\_OUT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="57cfd-137">Выходное значение.</span><span class="sxs-lookup"><span data-stu-id="57cfd-137">Output value.</span></span> <span data-ttu-id="57cfd-138">Функция записывает текущие параметры печати драйвера принтера, включая закрытые данные, в структуру данных [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , указанную параметром *пдевмодеаутпут* .</span><span class="sxs-lookup"><span data-stu-id="57cfd-138">The function writes the printer driver's current print settings, including private data, to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) data structure specified by the *pDevModeOutput* parameter.</span></span> <span data-ttu-id="57cfd-139">Вызывающий объект должен выделить буфер достаточно большим для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="57cfd-139">The caller must allocate a buffer sufficiently large to contain the information.</span></span> <span data-ttu-id="57cfd-140">Если двоичные **наборы \_ \_ буферов DM** отключены, параметр *пдевмодеаутпут* может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="57cfd-140">If the bit **DM\_OUT\_BUFFER** sets is clear, the *pDevModeOutput* parameter can be **NULL**.</span></span> <span data-ttu-id="57cfd-141">Это значение также определяется как **DM \_ Copy**.</span><span class="sxs-lookup"><span data-stu-id="57cfd-141">This value is also defined as **DM\_COPY**.</span></span><br/>                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57cfd-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="57cfd-142">Return value</span></span>

<span data-ttu-id="57cfd-143">Если параметр *фмоде* равен нулю, то возвращаемое значение представляет собой размер буфера, необходимого для хранения данных инициализации драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-143">If the *fMode* parameter is zero, the return value is the size of the buffer required to contain the printer driver initialization data.</span></span> <span data-ttu-id="57cfd-144">Обратите внимание, что этот буфер может быть больше, чем структура [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , если драйвер принтера добавляет закрытые данные в структуру.</span><span class="sxs-lookup"><span data-stu-id="57cfd-144">Note that this buffer can be larger than a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure if the printer driver appends private data to the structure.</span></span>

<span data-ttu-id="57cfd-145">Если функция отображает страницу свойств, возвращается значение либо **идок** , либо **идканцел**, в зависимости от выбранной пользователем кнопки.</span><span class="sxs-lookup"><span data-stu-id="57cfd-145">If the function displays the property sheet, the return value is either **IDOK** or **IDCANCEL**, depending on which button the user selects.</span></span>

<span data-ttu-id="57cfd-146">Если функция не отображает страницу свойств и завершается успешно, возвращается значение **идок**.</span><span class="sxs-lookup"><span data-stu-id="57cfd-146">If the function does not display the property sheet and is successful, the return value is **IDOK**.</span></span>

<span data-ttu-id="57cfd-147">Если функция завершается ошибкой, возвращаемое значение меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="57cfd-147">If the function fails, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="57cfd-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57cfd-148">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="57cfd-149">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="57cfd-149">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="57cfd-150">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="57cfd-150">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="57cfd-151">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="57cfd-151">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="57cfd-152">Строку, на которую указывает параметр *пдевиценаме* , можно получить путем вызова функции [**PrintOut**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="57cfd-152">The string pointed to by the *pDeviceName* parameter can be obtained by calling the [**GetPrinter**](getprinter.md) function.</span></span>

<span data-ttu-id="57cfd-153">Структура [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , которая фактически используется драйвером принтера, содержит независимую от устройства часть (как определено выше), за которой следует часть, относящаяся к драйверу, которая зависит от размера и содержимого с каждым драйвером и версией драйвера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-153">The [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure actually used by a printer driver contains the device-independent part (as defined above) followed by a driver-specific part that varies in size and content with each driver and driver version.</span></span> <span data-ttu-id="57cfd-154">Из-за этого зависимости от драйвера очень важно, чтобы приложения запрашивают драйвер для правильного размера структуры **DEVMODE** перед выделением для него буфера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-154">Because of this driver dependence, it is very important for applications to query the driver for the correct size of the **DEVMODE** structure before allocating a buffer for it.</span></span>

<span data-ttu-id="57cfd-155">**Чтобы изменить параметры печати, которые являются локальными для приложения, приложение должно выполнить следующие действия:**</span><span class="sxs-lookup"><span data-stu-id="57cfd-155">**To make changes to print settings that are local to an application, an application should follow these steps:**</span></span>

1.  <span data-ttu-id="57cfd-156">Получите число байтов, необходимых для полной структуры [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , вызвав **DocumentProperties** и указав ноль в параметре *фмоде* .</span><span class="sxs-lookup"><span data-stu-id="57cfd-156">Get the number of bytes required for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure by calling **DocumentProperties** and specifying zero in the *fMode* parameter.</span></span>
2.  <span data-ttu-id="57cfd-157">Выделите память для полной структуры [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="57cfd-157">Allocate memory for the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
3.  <span data-ttu-id="57cfd-158">Получите текущие параметры принтера, вызвав **DocumentProperties**.</span><span class="sxs-lookup"><span data-stu-id="57cfd-158">Get the current printer settings by calling **DocumentProperties**.</span></span> <span data-ttu-id="57cfd-159">Передайте указатель на структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , выделенную на шаге 2, в качестве параметра *пдевмодеаутпут* и укажите значение **\_ из \_ буфера DM out** .</span><span class="sxs-lookup"><span data-stu-id="57cfd-159">Pass a pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure allocated in Step 2 as the *pDevModeOutput* parameter and specify the **DM\_OUT\_BUFFER** value.</span></span>
4.  <span data-ttu-id="57cfd-160">Измените соответствующие члены возвращенной структуры [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) и укажите, какие члены были изменены, задав соответствующие биты в элементе **дмфиелдс** **DEVMODE**.</span><span class="sxs-lookup"><span data-stu-id="57cfd-160">Modify the appropriate members of the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure and indicate which members were changed by setting the corresponding bits in the **dmFields** member of the **DEVMODE**.</span></span>
5.  <span data-ttu-id="57cfd-161">Вызовите **DocumentProperties** и передайте измененную структуру [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) обратно в качестве параметров *пдевмодеинпут* и *пдевмодеаутпут* и укажите значения **\_ в полях \_ buffer** и **DM \_ out \_** (в сочетании с оператором OR). Структура **DEVMODE** , возвращаемая третьим вызовом **DocumentProperties** , может использоваться в качестве аргумента при вызове функции [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca) .</span><span class="sxs-lookup"><span data-stu-id="57cfd-161">Call **DocumentProperties** and pass the modified [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure back as both the *pDevModeInput* and *pDevModeOutput* parameters and specify both the **DM\_IN\_BUFFER** and **DM\_OUT\_BUFFER** values (which are combined using the OR operator).The **DEVMODE** structure returned by the third call to **DocumentProperties** can be used as an argument in a call to the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function.</span></span>

<span data-ttu-id="57cfd-162">Чтобы создать маркер для контекста устройства принтера с помощью текущих параметров принтера, необходимо вызвать **DocumentProperties** дважды, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="57cfd-162">To create a handle to a printer-device context using the current printer settings, you only need to call **DocumentProperties** twice, as described above.</span></span> <span data-ttu-id="57cfd-163">Первый вызов получает размер полного [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) , а второй вызывает инициализацию **DEVMODE** с использованием текущих параметров принтера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-163">The first call gets the size of the full [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) and the second call initializes the **DEVMODE** with the current printer settings.</span></span> <span data-ttu-id="57cfd-164">Передайте инициализированный **DEVMODE** в [**креатедк**](/windows/desktop/api/wingdi/nf-wingdi-createdca) , чтобы получить маркер контекста устройства принтера.</span><span class="sxs-lookup"><span data-stu-id="57cfd-164">Pass the initialized **DEVMODE** to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) to obtain the handle to the printer device context.</span></span>

## <a name="requirements"></a><span data-ttu-id="57cfd-165">Требования</span><span class="sxs-lookup"><span data-stu-id="57cfd-165">Requirements</span></span>



| <span data-ttu-id="57cfd-166">Требование</span><span class="sxs-lookup"><span data-stu-id="57cfd-166">Requirement</span></span> | <span data-ttu-id="57cfd-167">Значение</span><span class="sxs-lookup"><span data-stu-id="57cfd-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57cfd-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57cfd-168">Minimum supported client</span></span><br/> | <span data-ttu-id="57cfd-169">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57cfd-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="57cfd-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57cfd-170">Minimum supported server</span></span><br/> | <span data-ttu-id="57cfd-171">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57cfd-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="57cfd-172">Заголовок</span><span class="sxs-lookup"><span data-stu-id="57cfd-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="57cfd-173"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57cfd-173"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="57cfd-174">Библиотека</span><span class="sxs-lookup"><span data-stu-id="57cfd-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="57cfd-175"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57cfd-175"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="57cfd-176">DLL</span><span class="sxs-lookup"><span data-stu-id="57cfd-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57cfd-177"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="57cfd-177"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="57cfd-178">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="57cfd-178">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="57cfd-179">**Документпропертиесв** (Юникод) и **документпропертиеса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="57cfd-179">**DocumentPropertiesW** (Unicode) and **DocumentPropertiesA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="57cfd-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57cfd-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57cfd-181">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="57cfd-181">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="57cfd-182">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="57cfd-182">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="57cfd-183">**адванцеддокументпропертиес**</span><span class="sxs-lookup"><span data-stu-id="57cfd-183">**AdvancedDocumentProperties**</span></span>](advanceddocumentproperties.md)
</dt> <dt>

[<span data-ttu-id="57cfd-184">**креатедк**</span><span class="sxs-lookup"><span data-stu-id="57cfd-184">**CreateDC**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-createdca)
</dt> <dt>

[<span data-ttu-id="57cfd-185">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="57cfd-185">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="57cfd-186">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="57cfd-186">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="57cfd-187">**опенпринтер**</span><span class="sxs-lookup"><span data-stu-id="57cfd-187">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

