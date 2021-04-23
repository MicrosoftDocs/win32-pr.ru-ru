---
description: Создает объект контекста, описывающий указанное устройство планшета.
ms.assetid: 76f48485-a958-4457-9b87-73de73fa671e
title: 'Метод Итаблет:: CreateContext'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.CreateContext
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 9f1214f7f9e429b5f9b5b9614c2ccfc7fd1800b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912903"
---
# <a name="itabletcreatecontext-method"></a><span data-ttu-id="08348-103">Метод Итаблет:: CreateContext</span><span class="sxs-lookup"><span data-stu-id="08348-103">ITablet::CreateContext method</span></span>

<span data-ttu-id="08348-104">Создает объект контекста, описывающий указанное устройство планшета.</span><span class="sxs-lookup"><span data-stu-id="08348-104">Creates a context object that describes the specified tablet device.</span></span>

## <a name="syntax"></a><span data-ttu-id="08348-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08348-105">Syntax</span></span>


```C++
HRESULT CreateContext(
  [in]      HWND                    hWnd,
  [in]      RECT                    *prcInput,
  [in]      DWORD                   dwOptions,
  [in]      TABLET_CONTEXT_SETTINGS *pTCS,
  [in]      CONTEXT_ENABLE_TYPE     cet,
  [out]     ITabletContext          **ppCtx,
  [in, out] TABLET_CONTEXT_ID       *pTcid,
  [in, out] PACKET_DESCRIPTION      **ppPD,
  [in]      ITabletEventSink        *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="08348-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08348-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08348-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08348-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08348-108">Окно, к которому будет присоединен контекст планшета.</span><span class="sxs-lookup"><span data-stu-id="08348-108">The window to which the tablet context will be attached.</span></span>

</dd> <dt>

<span data-ttu-id="08348-109">*прЦинпут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08348-109">*prcInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08348-110">\[в уникальное\]</span><span class="sxs-lookup"><span data-stu-id="08348-110">\[in, unique\]</span></span>

<span data-ttu-id="08348-111">Прямоугольник ввода рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="08348-111">The ink input rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="08348-112">*двоптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08348-112">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08348-113">Флаги, устанавливающие параметры контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="08348-113">Flags that set tablet context options.</span></span>

</dd> <dt>

<span data-ttu-id="08348-114">*ПТКС* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08348-114">*pTCS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08348-115">\[в уникальное\]</span><span class="sxs-lookup"><span data-stu-id="08348-115">\[in, unique\]</span></span>

<span data-ttu-id="08348-116">Подробные сведения о создаваемом контексте планшета.</span><span class="sxs-lookup"><span data-stu-id="08348-116">Detailed information about the tablet context to create.</span></span>

</dd> <dt>

<span data-ttu-id="08348-117">*Центральноевропейское время* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08348-117">*cet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08348-118">Значение, которое включает или отключает сообщения контекста, отправляемые в окно.</span><span class="sxs-lookup"><span data-stu-id="08348-118">Value that enables or disables context messages being sent to the window.</span></span>

</dd> <dt>

<span data-ttu-id="08348-119">*ппкткс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="08348-119">*ppCtx* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08348-120">Указатель на только что созданный контекст планшета.</span><span class="sxs-lookup"><span data-stu-id="08348-120">A pointer to the newly create tablet context.</span></span>

</dd> <dt>

<span data-ttu-id="08348-121">*птЦид* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="08348-121">*pTcid* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08348-122">Значение, уникально идентифицирующее планшет.</span><span class="sxs-lookup"><span data-stu-id="08348-122">Value that uniquely identifies the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="08348-123">*пппд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="08348-123">*ppPD* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="08348-124">Указатель на сведения о том, какие данные содержатся в каждом пакете.</span><span class="sxs-lookup"><span data-stu-id="08348-124">Pointer to information about what data is contained in each packet.</span></span>

</dd> <dt>

<span data-ttu-id="08348-125">*псинк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="08348-125">*pSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08348-126">Объект [**итаблетевентсинк**](itableteventsink.md) , куда будут отправляться уведомления.</span><span class="sxs-lookup"><span data-stu-id="08348-126">The [**ITabletEventSink**](itableteventsink.md) object where notification messages will be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08348-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08348-127">Return value</span></span>

<span data-ttu-id="08348-128">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="08348-128">This method can return one of these values.</span></span>



| <span data-ttu-id="08348-129">Код возврата</span><span class="sxs-lookup"><span data-stu-id="08348-129">Return code</span></span>                                                                            | <span data-ttu-id="08348-130">Описание</span><span class="sxs-lookup"><span data-stu-id="08348-130">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="08348-131"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="08348-131"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="08348-132">Успешно.</span><span class="sxs-lookup"><span data-stu-id="08348-132">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="08348-133"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="08348-133"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="08348-134">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="08348-134">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="08348-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08348-135">Remarks</span></span>

<span data-ttu-id="08348-136">Как правило, приложение получает значения по умолчанию из [**метода итаблет:: жетдефаултконтекстсеттингс**](itablet-getdefaultcontextsettings.md), изменяет значения в соответствии с их потребностями, а затем передает измененную структуру параметров в **метод Итаблет:: CreateContext**.</span><span class="sxs-lookup"><span data-stu-id="08348-136">Typically, an application obtains the default values from the [**ITablet::GetDefaultContextSettings Method**](itablet-getdefaultcontextsettings.md), modifies values to suit their needs, and then passes the modified settings structure to the **ITablet::CreateContext Method**.</span></span>

> [!Note]  
> <span data-ttu-id="08348-137">При вызове **метода итаблет:: CreateContext** необходимо реализовать [**интерфейс итаблетевентсинк**](itableteventsink.md) .</span><span class="sxs-lookup"><span data-stu-id="08348-137">You must implement the [**ITabletEventSink Interface**](itableteventsink.md) when calling the **ITablet::CreateContext Method**.</span></span>

 

<span data-ttu-id="08348-138">Параметр *двоптионс* представляет собой набор битовых флагов, описывающих параметры контекста.</span><span class="sxs-lookup"><span data-stu-id="08348-138">The *dwOptions* parameter is a set of bit flags that describe context options.</span></span> <span data-ttu-id="08348-139">Эти флаги описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="08348-139">The following table describes these flags.</span></span>



| <span data-ttu-id="08348-140">Имя флага</span><span class="sxs-lookup"><span data-stu-id="08348-140">Flag Name</span></span>                                | <span data-ttu-id="08348-141">Значение</span><span class="sxs-lookup"><span data-stu-id="08348-141">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="08348-142">Описание</span><span class="sxs-lookup"><span data-stu-id="08348-142">Description</span></span>                                                                                                                                                                                                                                                              |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08348-143">ТККСО \_ поле</span><span class="sxs-lookup"><span data-stu-id="08348-143">TCXO\_MARGIN</span></span><br/>                  | <span data-ttu-id="08348-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="08348-144">0x00000001</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-145">Указывает, что входной контекст на планшете будет иметь поле.</span><span class="sxs-lookup"><span data-stu-id="08348-145">Specifies that the input context on the tablet will have a margin.</span></span> <span data-ttu-id="08348-146">Поле является областью за пределами заданной входной области, где события будут сопоставляться с границей области ввода.</span><span class="sxs-lookup"><span data-stu-id="08348-146">The margin is an area outside the specified input area where events will be mapped to the edge of the input area.</span></span> <span data-ttu-id="08348-147">Эта функция упрощает ввод точек на границе контекста.</span><span class="sxs-lookup"><span data-stu-id="08348-147">This feature makes it easier to input points at the edge of the context.</span></span><br/> |
| <span data-ttu-id="08348-148">\_ПРЕДобработчика ткксо</span><span class="sxs-lookup"><span data-stu-id="08348-148">TCXO\_PREHOOK</span></span><br/>                 | <span data-ttu-id="08348-149">0x00000002</span><span class="sxs-lookup"><span data-stu-id="08348-149">0x00000002</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-150">Предварительный обработчик получает пакеты перед обычными контекстами и обработчиками.</span><span class="sxs-lookup"><span data-stu-id="08348-150">Prehook gets packets before regular contexts and posthooks.</span></span> <span data-ttu-id="08348-151">Они получают пакеты в порядке их создания.</span><span class="sxs-lookup"><span data-stu-id="08348-151">They get packets in the order of their creation.</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="08348-152">\_состояние курсора ткксо \_</span><span class="sxs-lookup"><span data-stu-id="08348-152">TCXO\_CURSOR\_STATE</span></span><br/>           | <span data-ttu-id="08348-153">0x00000004</span><span class="sxs-lookup"><span data-stu-id="08348-153">0x00000004</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-154">TC вернет пакеты, даже если курсор работает.</span><span class="sxs-lookup"><span data-stu-id="08348-154">The TC will return packets even if the cursor is up.</span></span> <span data-ttu-id="08348-155">По умолчанию TC будет возвращать только те пакеты, когда курсор не работает.</span><span class="sxs-lookup"><span data-stu-id="08348-155">By default, a TC will only return packets when the cursor is down.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="08348-156">ТККСО \_ без \_ курсора \_</span><span class="sxs-lookup"><span data-stu-id="08348-156">TCXO\_NO\_CURSOR\_DOWN</span></span><br/>        | <span data-ttu-id="08348-157">0x00000008</span><span class="sxs-lookup"><span data-stu-id="08348-157">0x00000008</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-158">TC не возвращает пакеты, когда курсор не работает.</span><span class="sxs-lookup"><span data-stu-id="08348-158">The TC will not return packets when the cursor is down.</span></span><br/>                                                                                                                                                                                                       |
| <span data-ttu-id="08348-159">ТККСО \_ не \_ интегрирован</span><span class="sxs-lookup"><span data-stu-id="08348-159">TCXO\_NON\_INTEGRATED</span></span><br/>         | <span data-ttu-id="08348-160">0x00000010</span><span class="sxs-lookup"><span data-stu-id="08348-160">0x00000010</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-161">Контекст не будет интегрирован.</span><span class="sxs-lookup"><span data-stu-id="08348-161">The context will be non-integrated.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="08348-162">ТККСО- \_ обработчик</span><span class="sxs-lookup"><span data-stu-id="08348-162">TCXO\_POSTHOOK</span></span><br/>                | <span data-ttu-id="08348-163">0x00000020</span><span class="sxs-lookup"><span data-stu-id="08348-163">0x00000020</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-164">Обработчики получают пакеты после обычных контекстов планшета, но до контекста системы.</span><span class="sxs-lookup"><span data-stu-id="08348-164">Posthooks get packets after regular tablet contexts but before the system context.</span></span> <span data-ttu-id="08348-165">Они получают пакеты в порядке их создания.</span><span class="sxs-lookup"><span data-stu-id="08348-165">They get packets in the reverse order of their creation.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="08348-166">ТККСО \_ не \_ отобразить \_ курсор</span><span class="sxs-lookup"><span data-stu-id="08348-166">TCXO\_DONT\_SHOW\_CURSOR</span></span><br/>      | <span data-ttu-id="08348-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="08348-167">0x00000080</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-168">TC не установит позицию курсора.</span><span class="sxs-lookup"><span data-stu-id="08348-168">The TC will not set the cursor position.</span></span><br/>                                                                                                                                                                                                                      |
| <span data-ttu-id="08348-169">ТККСО \_ не \_ Проверка \_ TCS</span><span class="sxs-lookup"><span data-stu-id="08348-169">TCXO\_DONT\_VALIDATE\_TCS</span></span><br/>     | <span data-ttu-id="08348-170">0x00000100</span><span class="sxs-lookup"><span data-stu-id="08348-170">0x00000100</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-171">TC не будет проверять идентификаторы GUID, переданные в параметрах контекста планшета, на поддерживаемые свойства устройства.</span><span class="sxs-lookup"><span data-stu-id="08348-171">The TC will not validate the GUIDS passed in the tablet context settings against the supported properties of the device.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="08348-172">ТККСО \_ Разрешить \_ жесты</span><span class="sxs-lookup"><span data-stu-id="08348-172">TCXO\_ALLOW\_FLICKS</span></span><br/>           | <span data-ttu-id="08348-173">0x00000400</span><span class="sxs-lookup"><span data-stu-id="08348-173">0x00000400</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-174">TC допускает обнаружение жестов (по умолчанию это разрешено только в контекстах системы), и клиент будет получать \_ события многофункционального пера SE.</span><span class="sxs-lookup"><span data-stu-id="08348-174">The TC will allow flick detection to take place (by default this is only allowed on system contexts), and the client will get SE\_FLICK events.</span></span><br/>                                                                                                               |
| <span data-ttu-id="08348-175">ТККСО \_ Разрешить \_ \_ откасаний обратной связи</span><span class="sxs-lookup"><span data-stu-id="08348-175">TCXO\_ALLOW\_FEEDBACK\_TAPS</span></span><br/>   | <span data-ttu-id="08348-176">0x00000800</span><span class="sxs-lookup"><span data-stu-id="08348-176">0x00000800</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-177">TC разрешит отображение отзывов пера.</span><span class="sxs-lookup"><span data-stu-id="08348-177">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="08348-178">По умолчанию это разрешено только в контекстах системы.</span><span class="sxs-lookup"><span data-stu-id="08348-178">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="08348-179">ТККСО \_ Разрешить \_ обратную связь \_</span><span class="sxs-lookup"><span data-stu-id="08348-179">TCXO\_ALLOW\_FEEDBACK\_BARREL</span></span><br/> | <span data-ttu-id="08348-180">0x00001000</span><span class="sxs-lookup"><span data-stu-id="08348-180">0x00001000</span></span><br/>                                                                                                                                                                         | <span data-ttu-id="08348-181">TC разрешит отображение отзывов пера.</span><span class="sxs-lookup"><span data-stu-id="08348-181">The TC will allow pen feedback to be shown.</span></span> <span data-ttu-id="08348-182">По умолчанию это разрешено только в контекстах системы.</span><span class="sxs-lookup"><span data-stu-id="08348-182">By default, this is only allowed on system contexts.</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="08348-183">ТККСО \_ все</span><span class="sxs-lookup"><span data-stu-id="08348-183">TCXO\_ALL</span></span><br/>                     | <span data-ttu-id="08348-184">ТККСО \_ Margin \| ткксо предварительный \_ обработчик \| ткксо \_ состояние курсора \_ \| ткксо \_ без \_ курсора \_ \| ткксо \_ \_ неинтегрированный ткксо i- \| \_ перехватчик \| ткксо \_ не \_ отобразить \_ курсор \| ткксо \_ не \_ проверить \_ TCS</span><span class="sxs-lookup"><span data-stu-id="08348-184">TCXO\_MARGIN \| TCXO\_PREHOOK \| TCXO\_CURSOR\_STATE \| TCXO\_NO\_CURSOR\_DOWN \| TCXO\_NON\_INTEGRATED \| TCXO\_POSTHOOK \| TCXO\_DONT\_SHOW\_CURSOR \| TCXO\_DONT\_VALIDATE\_TCS</span></span><br/> | <span data-ttu-id="08348-185">Все определенные параметры контекста планшета.</span><span class="sxs-lookup"><span data-stu-id="08348-185">All defined tablet context options.</span></span><br/>                                                                                                                                                                                                                           |
| <span data-ttu-id="08348-186">\_обработчик ткксо</span><span class="sxs-lookup"><span data-stu-id="08348-186">TCXO\_HOOK</span></span><br/>                    | <span data-ttu-id="08348-187">ТККСО \_ ПРЕобработчика \| ткксо \_</span><span class="sxs-lookup"><span data-stu-id="08348-187">TCXO\_PREHOOK \| TCXO\_POSTHOOK</span></span><br/>                                                                                                                                                    | <span data-ttu-id="08348-188">Объединяет функции предварительного обработчика и после обработчика.</span><span class="sxs-lookup"><span data-stu-id="08348-188">Combines pre-hook and post-hook functionality.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="requirements"></a><span data-ttu-id="08348-189">Требования</span><span class="sxs-lookup"><span data-stu-id="08348-189">Requirements</span></span>



| <span data-ttu-id="08348-190">Требование</span><span class="sxs-lookup"><span data-stu-id="08348-190">Requirement</span></span> | <span data-ttu-id="08348-191">Значение</span><span class="sxs-lookup"><span data-stu-id="08348-191">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08348-192">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="08348-192">Minimum supported client</span></span><br/> | <span data-ttu-id="08348-193">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="08348-193">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="08348-194">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="08348-194">Minimum supported server</span></span><br/> | <span data-ttu-id="08348-195">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="08348-195">None supported</span></span><br/>                                                              |
| <span data-ttu-id="08348-196">Библиотека</span><span class="sxs-lookup"><span data-stu-id="08348-196">Library</span></span><br/>                  | <dl> <span data-ttu-id="08348-197"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08348-197"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08348-198">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08348-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08348-199">**Интерфейс Итаблет**</span><span class="sxs-lookup"><span data-stu-id="08348-199">**ITablet Interface**</span></span>](itablet.md)
</dt> <dt>

[<span data-ttu-id="08348-200">**\_ \_ Перечисление типов включения контекста**</span><span class="sxs-lookup"><span data-stu-id="08348-200">**CONTEXT\_ENABLE\_TYPE Enumeration**</span></span>](context-enable-type.md)
</dt> <dt>

[<span data-ttu-id="08348-201">**\_Структура параметров контекста планшета \_**</span><span class="sxs-lookup"><span data-stu-id="08348-201">**TABLET\_CONTEXT\_SETTINGS Structure**</span></span>](tablet-context-settings.md)
</dt> <dt>

[<span data-ttu-id="08348-202">**\_Структура описания пакета**</span><span class="sxs-lookup"><span data-stu-id="08348-202">**PACKET\_DESCRIPTION Structure**</span></span>](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_description)
</dt> <dt>

[<span data-ttu-id="08348-203">**Интерфейс Итаблетконтекстп**</span><span class="sxs-lookup"><span data-stu-id="08348-203">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> <dt>

[<span data-ttu-id="08348-204">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="08348-204">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




