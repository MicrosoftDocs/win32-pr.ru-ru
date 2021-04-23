---
description: Эксперт должен реализовать функцию Run. Сетевой монитор вызывает функцию Run для запуска эксперта в библиотеке DLL эксперта.
ms.assetid: 9ef3941b-d9e9-4acb-97ed-5f39573f2946
title: Запуск функции обратного вызова (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Run
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: c2dff2cf70a6d989928f17447fa3491dd9509f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897666"
---
# <a name="run-callback-function"></a><span data-ttu-id="c22b5-104">Запустить функцию обратного вызова</span><span class="sxs-lookup"><span data-stu-id="c22b5-104">Run callback function</span></span>

<span data-ttu-id="c22b5-105">Эксперт должен реализовать функцию **Run** .</span><span class="sxs-lookup"><span data-stu-id="c22b5-105">The expert must implement the **Run** function.</span></span> <span data-ttu-id="c22b5-106">Сетевой монитор вызывает функцию **Run** для запуска эксперта в библиотеке DLL эксперта.</span><span class="sxs-lookup"><span data-stu-id="c22b5-106">Network Monitor calls the **Run** function to start the expert within the expert DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="c22b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c22b5-107">Syntax</span></span>


```C++
BOOL WINAPI Run(
  _In_ HEXPERTKEY         hExpertKey,
  _In_ PEXPERTCONFIG      pConfig,
  _In_ PEXPERTSTARTUPINFO pExpertStartupInfo,
  _In_ DWORD              StartupFlags,
  _In_ HWND               hWndParent
);
```



## <a name="parameters"></a><span data-ttu-id="c22b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c22b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c22b5-109">*хексперткэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-109">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22b5-110">Уникальный идентификатор эксперта, который передается обратно в сетевой монитор функции, относящиеся к экспертам.</span><span class="sxs-lookup"><span data-stu-id="c22b5-110">Unique identifier of the expert that is passed back to all expert-specific Network Monitor functions.</span></span>

> [!Note]  
> <span data-ttu-id="c22b5-111">Идентификатор *хексперткэй* может передавать экспертный ключ, отличный от экспертного ключа, который передает функция [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="c22b5-111">The *hExpertKey* identifier may pass an expert key that is different from the expert key that the [**Configure**](configure.md) function passes.</span></span>

 

</dd> <dt>

<span data-ttu-id="c22b5-112">*pConfig* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-112">*pConfig* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22b5-113">Указатель на существующую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="c22b5-113">Pointer to the existing configuration.</span></span> <span data-ttu-id="c22b5-114">Параметр *pConfig* может иметь **значение NULL** , что означает, что эксперт может работать с жестко заданными значениями по умолчанию или со сведениями о запуске, на которые ссылается параметр *пекспертстартупинфо* .</span><span class="sxs-lookup"><span data-stu-id="c22b5-114">The *pConfig* parameter may be **NULL** which means that the expert can run with hard-coded defaults, or startup information that the *pExpertStartupInfo* parameter references.</span></span>

</dd> <dt>

<span data-ttu-id="c22b5-115">*пекспертстартупинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-115">*pExpertStartupInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22b5-116">Указатель на элемент захвата, имеющий фокус при запуске эксперта.</span><span class="sxs-lookup"><span data-stu-id="c22b5-116">Pointer to the capture element that has focus when the expert starts.</span></span>

</dd> <dt>

<span data-ttu-id="c22b5-117">*Стартупфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-117">*StartupFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22b5-118">Признак использования параметра *пекспертстартупинфо* экспертом.</span><span class="sxs-lookup"><span data-stu-id="c22b5-118">Indicator for how the expert should use the *pExpertStartupInfo* parameter.</span></span>

<span data-ttu-id="c22b5-119">Единственный заданный флаг:</span><span class="sxs-lookup"><span data-stu-id="c22b5-119">The only flag defined is:</span></span>



| <span data-ttu-id="c22b5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="c22b5-120">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="c22b5-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c22b5-121">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EXPERT_STARTUP_FLAG_USE_STARTUP_DATA_OVER_CONFIG_DATA."></span><span id="expert_startup_flag_use_startup_data_over_config_data."></span><dl> <span data-ttu-id="c22b5-122"><dt>**\_флаг запуска эксперта \_ \_ использование \_ загрузочных \_ данных \_ для \_ \_ данных конфигурации.**</dt></span><span class="sxs-lookup"><span data-stu-id="c22b5-122"><dt>**EXPERT\_STARTUP\_FLAG\_USE\_STARTUP\_DATA\_OVER\_CONFIG\_DATA.**</dt></span></span> </dl> | <span data-ttu-id="c22b5-123">Этот флаг указывает, что эксперт использует параметр *пекспертстартупинфо* и не использует параметр *pConfig* .</span><span class="sxs-lookup"><span data-stu-id="c22b5-123">This flag indicates that the expert uses the *pExpertStartupInfo* parameter, and does not use the *pConfig* parameter.</span></span> <span data-ttu-id="c22b5-124">Как правило, этот флаг можно установить, когда эксперт может начать с щелчка правой кнопкой мыши.</span><span class="sxs-lookup"><span data-stu-id="c22b5-124">Typically, you can set this flag when the expert can start from a right-mouse click.</span></span> <span data-ttu-id="c22b5-125">Если флаг не установлен, возможны следующие два действия: либо эксперт не начинает с щелчка правой кнопкой мыши, либо эксперт начинает с щелчка правой кнопкой мыши, а затем пользователь настраивает его.</span><span class="sxs-lookup"><span data-stu-id="c22b5-125">If the flag is not set, the following two things can occur: either the expert does not start from a right-mouse click, or the expert starts from a right-mouse click, and then the user configures it.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c22b5-126">*хвндпарент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-126">*hWndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22b5-127">Параметр *HWND* родительского элемента (обычно это сетевой монитор пользовательский интерфейс).</span><span class="sxs-lookup"><span data-stu-id="c22b5-127">The *hWnd* parameter of the parent (usually the Network Monitor user interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c22b5-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c22b5-128">Return value</span></span>

<span data-ttu-id="c22b5-129">Если функция выполнена успешно (то есть при запуске эксперта), возвращается значение **true**.</span><span class="sxs-lookup"><span data-stu-id="c22b5-129">If the function is successful (that is, if the expert starts), the return value is **TRUE**.</span></span>

<span data-ttu-id="c22b5-130">Если функция завершается неудачно, возвращается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="c22b5-130">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c22b5-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c22b5-131">Remarks</span></span>

<span data-ttu-id="c22b5-132">При запуске эксперт просматривает кадры в файле записи и либо создает отчет, либо создает события, которые показывают проблемы.</span><span class="sxs-lookup"><span data-stu-id="c22b5-132">When running, the expert loops through the frames in the capture file and either generates a report or creates events that show problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="c22b5-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c22b5-133">Requirements</span></span>



| <span data-ttu-id="c22b5-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c22b5-134">Requirement</span></span> | <span data-ttu-id="c22b5-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c22b5-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c22b5-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c22b5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c22b5-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c22b5-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c22b5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c22b5-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c22b5-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c22b5-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c22b5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c22b5-141"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c22b5-141"><dt>Netmon.h</dt></span></span> </dl> |



 

 




