---
description: Настраивает эксперт в библиотеке DLL эксперта.
ms.assetid: 3906569d-9ad4-4c03-9637-f4a57697b227
title: Настройка функции обратного вызова (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Configure
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 76ba55b7544e35a07b74a41788a3befa766f87bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663026"
---
# <a name="configure-callback-function"></a><span data-ttu-id="be716-103">Настройка функции обратного вызова</span><span class="sxs-lookup"><span data-stu-id="be716-103">Configure callback function</span></span>

<span data-ttu-id="be716-104">Функция **Configure** настраивает эксперт в библиотеке DLL эксперта.</span><span class="sxs-lookup"><span data-stu-id="be716-104">The **Configure** function configures the expert within the expert DLL.</span></span>

<span data-ttu-id="be716-105">Эксперт должен реализовать функцию **Configure** .</span><span class="sxs-lookup"><span data-stu-id="be716-105">The expert must implement the **Configure** function.</span></span> <span data-ttu-id="be716-106">При получении вызова функции эксперт отображает диалоговое окно, позволяющее пользователю изменять любой настраиваемый элемент.</span><span class="sxs-lookup"><span data-stu-id="be716-106">When the function call is received, the expert displays a dialog box that enables the user to change any configurable item.</span></span>

## <a name="syntax"></a><span data-ttu-id="be716-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be716-107">Syntax</span></span>


```C++
BOOL WINAPI Configure(
  _In_    HEXPERTKEY         hExpertKey,
  _Inout_ PEXPERTCONFIG      *ppConfig,
  _In_    PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_    DWORD              StartupFlags,
  _In_    HWND               hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="be716-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="be716-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be716-109">*хексперткэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be716-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be716-110">Уникальный идентификатор эксперта.</span><span class="sxs-lookup"><span data-stu-id="be716-110">Unique expert identifier.</span></span>

<span data-ttu-id="be716-111">Уникальный идентификатор передается обратно для всех функций сетевой монитор, зависящих от эксперта.</span><span class="sxs-lookup"><span data-stu-id="be716-111">The unique identifier is passed back on all expert-specific Network Monitor functions.</span></span> <span data-ttu-id="be716-112">Имейте в виду, что идентификатор может не совпадать с ключом эксперта, который был передан функции [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="be716-112">Be aware that the identifier may not be the same expert key as the one passed to the [**Run**](run.md) function.</span></span> <span data-ttu-id="be716-113">Не храните ключ эксперта в вызове **Configure** .</span><span class="sxs-lookup"><span data-stu-id="be716-113">Do not store the expert key from the **Configure** call.</span></span>

</dd> <dt>

<span data-ttu-id="be716-114">*ппконфиг* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="be716-114">*ppConfig* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="be716-115">Указатель на указатель на структуру [**експертконфиг**](expertconfig.md) после записи.</span><span class="sxs-lookup"><span data-stu-id="be716-115">A pointer to a pointer to an [**EXPERTCONFIG**](expertconfig.md) structure upon entry.</span></span>

<span data-ttu-id="be716-116">После успешного выхода структура [**експертконфиг**](expertconfig.md) , на которую указывает ссылка, содержит новые данные конфигурации.</span><span class="sxs-lookup"><span data-stu-id="be716-116">After a successful exit, the referenced [**EXPERTCONFIG**](expertconfig.md) structure contains the new configuration data.</span></span>

</dd> <dt>

<span data-ttu-id="be716-117">*пекспертстартупинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be716-117">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be716-118">Указатель на элемент захвата с фокусом при запуске эксперта.</span><span class="sxs-lookup"><span data-stu-id="be716-118">A pointer to the capture element with focus when the expert started.</span></span>

</dd> <dt>

<span data-ttu-id="be716-119">*Стартупфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be716-119">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be716-120">Флаги, указывающие, как эксперт должен использовать параметр *пекспертстартупинфо* .</span><span class="sxs-lookup"><span data-stu-id="be716-120">The flags that indicate how the expert should use the *pExpertStartupInfo* parameter.</span></span> <span data-ttu-id="be716-121">Единственный заданный флаг — это **флаг запуска "Эксперт". \_ \_ \_ Используйте данные о \_ загрузке \_ \_ для \_ \_ данных конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="be716-121">The only flag defined is **EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA**.</span></span> <span data-ttu-id="be716-122">Флаг указывает, что эксперт будет использовать параметр *пекспертстартупинфо* , а не переданный параметр *ппконфиг* .</span><span class="sxs-lookup"><span data-stu-id="be716-122">The flag indicates that the expert will use the *pExpertStartupInfo* parameter rather than the *ppConfig* parameter that passed in.</span></span> <span data-ttu-id="be716-123">Обычно флаг задается при запуске эксперта из контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="be716-123">Typically, you set the flag when you start the expert from a context menu.</span></span>

</dd> <dt>

<span data-ttu-id="be716-124">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="be716-124">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be716-125">Маркер родительского окна.</span><span class="sxs-lookup"><span data-stu-id="be716-125">A handle to the parent window.</span></span> <span data-ttu-id="be716-126">Используйте маркер, чтобы открыть диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="be716-126">Use the handle to open a dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be716-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be716-127">Return value</span></span>

<span data-ttu-id="be716-128">Если функция выполнена успешно (то есть, если текущая конфигурация существует), возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="be716-128">If the function is successful (that is, if a current configuration exists), the return value is **TRUE**.</span></span>

<span data-ttu-id="be716-129">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="be716-129">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="be716-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be716-130">Remarks</span></span>

<span data-ttu-id="be716-131">Сетевой монитор вызывает функцию **Configure** с текущей конфигурацией эксперта, если она существует.</span><span class="sxs-lookup"><span data-stu-id="be716-131">Network Monitor calls the **Configure** function with the current configuration of the expert, if one exists.</span></span> <span data-ttu-id="be716-132">Эксперт отображает диалоговое окно, в котором можно изменить любой настраиваемый элемент.</span><span class="sxs-lookup"><span data-stu-id="be716-132">The expert displays a dialog box, with which you can change any configurable item.</span></span>

<span data-ttu-id="be716-133">Если *ппконфиг* передается и сетевой монитор не имеет конфигурации, хранящейся для указанного эксперта, значение параметра может быть **равно NULL**.</span><span class="sxs-lookup"><span data-stu-id="be716-133">When *ppConfig* is passed in and Network Monitor does not have a configuration stored for the specified expert, the parameter value can be **NULL**.</span></span> <span data-ttu-id="be716-134">В этом случае функция **Configure** принимает жестко запрограммированные значения по умолчанию (или использует сведения о запуске) для открытия диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="be716-134">In this case, the **Configure** function assumes hard-coded default values (or, uses the startup information) to open the dialog box.</span></span>

<span data-ttu-id="be716-135">Данные конфигурации также могут иметь **значение NULL** , если функция **Configure** возвращает, а **значение NULL** было передано.</span><span class="sxs-lookup"><span data-stu-id="be716-135">The configuration data can also be **NULL** when the **Configure** function returns, and a **NULL** was passed-in.</span></span> <span data-ttu-id="be716-136">Такая ситуация возникает, когда сетевой монитор не имеет сохраненного значения по умолчанию и пользователь нажимает кнопку **Отмена**.</span><span class="sxs-lookup"><span data-stu-id="be716-136">This situation occurs when Network Monitor does not have a stored default, and the user presses **Cancel**.</span></span>

<span data-ttu-id="be716-137">В начале структуры данных [**експертконфиг**](expertconfig.md) входит частный раздел, в котором хранятся сведения о размере структуры.</span><span class="sxs-lookup"><span data-stu-id="be716-137">The beginning of the [**EXPERTCONFIG**](expertconfig.md) data structure includes a Private section that stores the structure size information.</span></span> <span data-ttu-id="be716-138">Размер структуры **експертконфиг** должен включать зарезервированную длину **DWORD** , которая отображается в начале структуры.</span><span class="sxs-lookup"><span data-stu-id="be716-138">The size of the **EXPERTCONFIG** structure should include the reserved **DWORD** length that appears at the beginning of the structure.</span></span> <span data-ttu-id="be716-139">Например, если для данных конфигурации требуется 20 байт дискового пространства, выделите 24 байта для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="be716-139">For example, if your configuration data requires 20 bytes of storage space, allocate 24 bytes to store the data.</span></span> <span data-ttu-id="be716-140">Если *ппконфиг* имеет **значение NULL**, функция **Configure** вызывает функцию [**експерталлокмемори**](expertallocmemory.md) для выделения новой конфигурации, которая имеет правильный размер.</span><span class="sxs-lookup"><span data-stu-id="be716-140">If a *ppConfig* is **NULL**, the **Configure** function calls the [**ExpertAllocMemory**](expertallocmemory.md) function to allocate a new configuration that is the correct size.</span></span> <span data-ttu-id="be716-141">Если буфер недостаточно для хранения данных экспертов, эксперт должен вызвать функцию [**експертреаллокмемори**](expertreallocmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="be716-141">If the buffer is not enough to hold the expert data, the expert should call the [**ExpertReallocMemory**](expertreallocmemory.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="be716-142">Требования</span><span class="sxs-lookup"><span data-stu-id="be716-142">Requirements</span></span>



| <span data-ttu-id="be716-143">Требование</span><span class="sxs-lookup"><span data-stu-id="be716-143">Requirement</span></span> | <span data-ttu-id="be716-144">Значение</span><span class="sxs-lookup"><span data-stu-id="be716-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="be716-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be716-145">Minimum supported client</span></span><br/> | <span data-ttu-id="be716-146">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be716-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="be716-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be716-147">Minimum supported server</span></span><br/> | <span data-ttu-id="be716-148">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be716-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="be716-149">Заголовок</span><span class="sxs-lookup"><span data-stu-id="be716-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="be716-150"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="be716-150"><dt>Netmon.h</dt></span></span> </dl> |



 

 




