---
title: Проходы рендеринга Direct3D 12
description: Функция передачи прорисовки позволяет повысить эффективность работы графического процессора за счет уменьшения трафика памяти в память и из нее. Это позволяет приложению лучше выявляет требования к подготовке к просмотру ресурсов и зависимости данных.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: 96ed14cecd518a3e03672f2667306ee0a4b8d64999aab01aa72aae04975f0a83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069694"
---
# <a name="direct3d-12-render-passes"></a>Проходы рендеринга Direct3D 12

функция подготовки к просмотру является новой для Windows 10, версия 1809 (10,0; Сборка 17763) и содержит концепцию прохода визуализации Direct3D 12. Проход визуализации состоит из подмножества команд, записанных в список команд.

Чтобы объявить, где начинается и заканчивается каждый проход рендеринга, вы вкладывает команды, относящиеся к этому проходу, внутри вызовов [**ID3D12GraphicsCommandList4:: бегинрендерпасс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass) и [**ендрендерпасс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-endrenderpass). Следовательно, любой список команд содержит ноль, один или несколько проходов рендеринга.

## <a name="scenarios"></a>Сценарии

Проходы рендеринга могут повысить производительность модуля подготовки отчетов, если он основан на Tile-Based отложенной отрисовки (ТБДР), помимо других методов. В частности, этот метод позволяет модулю подготовки отчетов повысить эффективность работы GPU за счет уменьшения трафика памяти в и из памяти, позволяя приложению лучше обнаруживать требования к подготовке к просмотру ресурсов и зависимости данных.

Отображаемый драйвер, написанный явным образом для использования функции прорисовки, дает лучшие результаты. Но подготовка к просмотру интерфейсов API может выполняться даже на уже существующих драйверах (хотя, не обязательно с повышением производительности).

Это сценарии, в которых проходы рендеринга предназначены для предоставления значения.

### <a name="allow-your-application-to-avoid-unnecessary-loadsstores-of-resources-fromto-main-memory-on-a-tile-based-deferred-rendering-tbdr-architecture"></a>Разрешите приложению избежать ненужных нагрузок или хранилищ ресурсов в основной памяти на Tile-Based архитектуре отложенной отрисовки (ТБДР)

Одно из значений этапов отрисовки — это то, что оно предоставляет централизованное расположение зависимостей данных приложения для набора операций отрисовки. Эти зависимости данных позволяют драйверу экрана проверять эти данные в течение времени привязки или барьера, а также выдавать инструкции, которые уменьшают загрузку ресурсов и сохраняет их в основной памяти.

### <a name="allow-your-tbdr-architecture-to-opportunistically-persistent-resources-in-on-chip-cache-across-render-passes-even-in-separate-command-lists"></a>Разрешите вашей архитектуре ТБДР рационально постоянные ресурсы в кэше в микросхеме для проходов отрисовки (даже в отдельных списках команд).

> [!NOTE]
> В частности, этот сценарий ограничивается ситуациями, когда вы пишете в одни и те же целевые объекты отрисовки в нескольких списках команд.

Общий шаблон отрисовки предназначен для того, чтобы приложение отображалось в одни и те же целевые объекты отрисовки для нескольких списков команд последовательно, даже несмотря на то, что команды отрисовки создаются параллельно. Использование проходов рендеринга в этом сценарии позволяет объединять эти передачи таким образом (так как приложение знает, что оно будет возобновлять отрисовку в списке команд сразу же), что драйвер экрана может избежать сброса в основную память в границах списка команд.

## <a name="your-applications-responsibilities"></a>Обязанности приложения

Даже при использовании функции «прорисовка», ни среда выполнения Direct3D 12, ни видеодрайвер не принимают на себя ответственность за вывод возможностей по переупорядочиванию и предотвращению загрузки и хранения. Чтобы правильно использовать функцию передачи прорисовки, приложение имеет эти обязанности.

- Правильно выявление зависимостей данных и упорядочения для своих операций.
- Упорядочивайте свои отклонения таким образом, чтобы свести к сведению сокращение количества записей на диск (поэтому, сократите использование флагов **_PRESERVE** ).
- Правильно используйте барьеры ресурсов и следите за состоянием ресурсов.
- Избегайте ненужных копий и сбросов. чтобы определить их, можно использовать автоматические предупреждения о производительности из [средства PIX on Windows tool](https://devblogs.microsoft.com/pix/).

## <a name="using-the-render-pass-feature"></a>Использование функции «подготовка к просмотру»

### <a name="what-is-a-render-pass"></a>Что такое *проход прорисовки*?

Проход визуализации определяется этими элементами.

- Набор выходных привязок, фиксированных на протяжении этапа подготовки к просмотру. Эти привязки относятся к одному или нескольким представлениям целевого объекта отрисовки (RTVs) и (или) к представлению трафарета глубины.
- Список операций GPU, предназначенных для набора выходных привязок.
- Метаданные, описывающие зависимости нагрузки и хранения для всех выходных привязок, предназначенных для прохода визуализации.

### <a name="declare-your-output-bindings"></a>Объявление выходных привязок

В начале этапа рендеринга вы объявляете привязки для целевых объектов отрисовки и (или) в буфер глубины или шаблона. Привязка к целевым объекту отрисовки необязательна, и она необязательна для привязки к буферу глубины или шаблона. Однако необходимо выполнить привязку по крайней мере к одному из двух, а в приведенном ниже примере кода выполнить привязку к обоим.

Эти привязки объявляются в вызове [**ID3D12GraphicsCommandList4:: бегинрендерпасс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass).

```cppwinrt
void render_passes(::ID3D12GraphicsCommandList4 * pIGCL4,
    D3D12_CPU_DESCRIPTOR_HANDLE const& rtvCPUDescriptorHandle,
    D3D12_CPU_DESCRIPTOR_HANDLE const& dsvCPUDescriptorHandle)
{
    const float clearColor4[]{ 0.f, 0.f, 0.f, 0.f };
    CD3DX12_CLEAR_VALUE clearValue{ DXGI_FORMAT_R32G32B32_FLOAT, clearColor4 };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessClear{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR, { clearValue } };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessPreserve{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_PRESERVE, {} };
    D3D12_RENDER_PASS_RENDER_TARGET_DESC renderPassRenderTargetDesc{ rtvCPUDescriptorHandle, renderPassBeginningAccessClear, renderPassEndingAccessPreserve };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessNoAccess{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessNoAccess{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_DEPTH_STENCIL_DESC renderPassDepthStencilDesc{ dsvCPUDescriptorHandle, renderPassBeginningAccessNoAccess, renderPassBeginningAccessNoAccess, renderPassEndingAccessNoAccess, renderPassEndingAccessNoAccess };

    pIGCL4->BeginRenderPass(1, &renderPassRenderTargetDesc, &renderPassDepthStencilDesc, D3D12_RENDER_PASS_FLAG_NONE);
    // Record command list.
    pIGCL4->EndRenderPass();
    // Begin/End further render passes and then execute the command list(s).
}
```

Первое поле структуры [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) задается дескриптору дескриптора ЦП, соответствующему одному или нескольким представлениям целевого объекта отрисовки (RTVs). Аналогично [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) содержит дескриптор ДЕСКРИПТОРа ЦП, соответствующий представлению трафарета глубины (DSV). Дескрипторы дескрипторов ЦП являются теми же, которые в противном случае передавались в [**ID3D12GraphicsCommandList:: омсетрендертаржетс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets). И, как и в случае с **омсетрендертаржетс**, ДЕСКРИПТОРы ЦП *привязываются* из соответствующих куч (дескрипторов ЦП) во время вызова **бегинрендерпасс**.

RTVs и DSV не наследуются в ходе подготовки к просмотру. Вместо этого они должны быть установлены. Кроме того, RTVs и DSV, объявленные в **бегинрендерпасс** , распространяются в список команд. Вместо этого они находятся в неопределенном состоянии после этапа подготовки к просмотру.

### <a name="render-passes-and-workloads"></a>Этапы отрисовки и рабочие нагрузки

Нельзя вложить проходы рендеринга, и вы не сможете выполнить проход рендеринга в нескольких списках команд (они должны начинаться и заканчиваться при записи в один список команд). Оптимизация, предназначенная для реализации эффективного многопоточного создания проходов рендеринга, обсуждается в разделе [ Подготовка флагов передачи](#render-pass-flags)ниже.

Запись, которую вы выполняете в ходе передачи, не является *допустимой* для чтения до последующего прохода отрисовки. Это исключает некоторые типы барьеров в рамках прохода рендеринга &mdash; , например, барьер от **RENDER_TARGET** до **SHADER_RESOURCE** на целевом объекте отрисовки, привязанном в текущий момент. Дополнительные сведения см. в разделе [этапы подготовки к просмотру и барьеры ресурсов](#render-passes-and-resource-barriers)ниже.

Единственным исключением в ограничении записи и чтения, которое было упомянуто выше, является неявное считывание, которое выполняется в процессе тестирования глубины и наложения целевого объекта визуализации.
Таким образом, эти API запрещены в рамках прохода отрисовки (основная среда выполнения удаляет список команд, если они вызываются во время записи).

- [**ID3D12GraphicsCommandList1:: Атомиккопибуфферуинт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)
- [**ID3D12GraphicsCommandList4:: Бегинрендерпасс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass)
- [**ID3D12GraphicsCommandList:: КлеардепсстенЦилвиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
- [**ID3D12GraphicsCommandList:: Клеаррендертаржетвиев**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
- [**ID3D12GraphicsCommandList:: Клеарстате**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
- [**ID3D12GraphicsCommandList:: Клеарунордередакцессвиевфлоат**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
- [**ID3D12GraphicsCommandList:: Клеарунордередакцессвиевуинт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
- [**ID3D12GraphicsCommandList:: Копибуфферрегион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
- [**ID3D12GraphicsCommandList:: Копиресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
- [**ID3D12GraphicsCommandList:: Копитекстуререгион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
- [**ID3D12GraphicsCommandList:: Копитилес**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
- [**ID3D12GraphicsCommandList::D Искардресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
- [**ID3D12GraphicsCommandList::D Patch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
- [**ID3D12GraphicsCommandList:: Омсетрендертаржетс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
- [**ID3D12GraphicsCommandList:: Ресолвекуеридата**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
- [**ID3D12GraphicsCommandList:: Ресолвесубресаурце**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
- [**ID3D12GraphicsCommandList1:: Ресолвесубресаурцерегион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion)
- [**ID3D12GraphicsCommandList3:: Сетпротектедресаурцесессион**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist3-setprotectedresourcesession)

### <a name="render-passes-and-resource-barriers"></a>Этапы рендеринга и барьеры ресурсов

Вы не можете читать или использовать запись, которая произошла в рамках одного этапа рендеринга. Некоторые барьеры не соответствуют этому ограничению, например от **D3D12_RESOURCE_STATE_RENDER_TARGET** до **\* _SHADER_RESOURCE** на целевом объекте отрисовки в данный момент (и уровень отладки приведет к ошибке). Но такое же барьер на целевом объекте прорисовки, записанном *вне* текущего прохода отрисовки, является согласованным, так как операции записи будут завершаться до начала текущего прохода отрисовки.
Вам может быть полезно знать о некоторых оптимизациях, которые могут быть внесены драйвером экрана в этом отношении. При наличии согласованной рабочей нагрузки драйвер экрана может перемещать любые барьеры, обнаруженные в процессе подготовки к просмотру, в начало прохода рендеринга. Там они могут быть объединены (и не влияют на операции заполнения или группирования). Это допустимая оптимизация, при которой все операции записи были завершены до начала текущего прохода рендеринга.

Ниже приведен пример более полного примера оптимизации драйверов, в котором предполагается, что у вас есть механизм визуализации, имеющий архитектуру привязки ресурсов до Direct3D 12, &mdash; выполняющую барьеры по *запросу в* зависимости от того, как привязаны ресурсы. При записи в представление неупорядоченного доступа (UAV) к концу кадра (для использования в следующем фрейме) обработчик может оставить ресурс в состоянии **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** в конце кадра. В следующем фрейме, когда обработчик привязывает ресурс как представление ресурсов шейдера (SRV), он обнаружит, что ресурс находится в неправильном состоянии, и он выдаст барьер от **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** до **D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE**. Если это барьер находится на этапе подготовки к просмотру, то драйвер экрана выключается в том случае, если все операции записи уже выполнялись *за пределами* текущего прохода отрисовки, и соответственно (и при этом происходит оптимизация). видеодрайвер может *переместить* барьер вплоть до начала этапа подготовки к просмотру. Опять же, это допустимо, пока код соответствует ограничению «запись-чтение», описанному в этом разделе и последнем.


Это примеры согласованных барьеров.
- **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** **D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**.
- **D3D12_RESOURCE_STATE_COPY_DEST** **\* _SHADER_RESOURCE**.

И это примеры несогласованных препятствий.

- **D3D12_RESOURCE_STATE_RENDER_TARGET** в любое состояние чтения в RTVs/DSV, привязанном к текущему объекту.
- **D3D12_RESOURCE_STATE_DEPTH_WRITE** в любое состояние чтения в RTVs/DSV, привязанном к текущему объекту.
- Любой барьер для псевдонимов.
- Неупорядоченные барьеры представления доступа (UAV). 

### <a name="resource-access-declaration"></a>Объявление доступа к ресурсам

Во время **бегинрендерпасс** , а также объявление всех ресурсов, которые обслуживаются в качестве RTVs и (или) представления источника данных в рамках этого прохода, необходимо также указать их начальные и конечные характеристики *доступа* . Как можно увидеть в примере кода в разделе [объявление выходных привязок](#declare-your-output-bindings) выше, это можно сделать с помощью структур [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) и [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) .

Дополнительные сведения см. в разделе структуры [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access) и [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access) , а также перечисления [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type) и [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type) .

### <a name="render-pass-flags"></a>Отрисовывает флаги Pass

Последний параметр, переданный в **бегинрендерпасс** , является флагом этапа подготовки к просмотру (значение из перечисления [**D3D12_RENDER_PASS_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_flags) ).

```cppwinrt
enum D3D12_RENDER_PASS_FLAGS
{
    D3D12_RENDER_PASS_FLAG_NONE = 0,
    D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES = 0x1,
    D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS = 0x2,
    D3D12_RENDER_PASS_FLAG_RESUMING_PASS = 0x4
};
```

#### <a name="uav-writes-within-a-render-pass"></a>UAV записи в рамках прохода прорисовки

Операции записи неупорядоченного представления доступа (UAV) разрешены в рамках этапа подготовки к просмотру, но необходимо указать, что вы будете выдавать UAV записи в рамках прохода визуализации, указав **D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES**, чтобы драйвер дисплея мог отказаться от мозаичного заполнения при необходимости.

UAVные обращения должны следовать описанному выше ограничению Write-Read (операции записи в ходе подготовки к просмотру недопустимы для чтения до последующего прохода отрисовки). UAV барьеры не разрешены в рамках прохода рендеринга.

Привязки UAV (с помощью корневых таблиц или корневых дескрипторов) наследуются в проходы прорисовки и распространяются из проходов прорисовки.

#### <a name="suspending-passes-and-resuming-passes"></a>Приостановка — передача и возобновление — пройденные

Можно указать весь проход отрисовки как приостановку и/или возобновление-проход. Приостановка-последующего связывания должно иметь идентичные представления и флаги доступа между проходами, и могут не иметь каких-либо промежуточных операций GPU (например, прорисовка, отправка, Отмена, очистка, копирование, сопоставление элементов обновления, немедленный режим записи, запросы, разрешения запросов) между приостановкой этапа подготовки к просмотру и возобновлением прохода визуализации.

Предполагаемый вариант использования — многопоточный рендеринг, где, например, четыре списка команд (каждый с собственными проходами рендеринга) могут ориентироваться на одни и те же целевые объекты рендеринга. Когда проходы прорисовки приостановлены или возобновляются в списках команд, списки команд должны выполняться в том же вызове [**ID3D12CommandQueue:: ексекутекоммандлистс**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Проход рендеринга может возобновляться и приостанавливаться. В многопоточном примере, в котором указаны списки команд 2 и 3, будут возобновлены с 1 до 2 соответственно. И в то же время 2 и 3 приостанавливаются к 3 и 4 соответственно.

## <a name="query-for-render-passes-feature-support"></a>Запрос на поддержку функций функции подготовки к просмотру

Можно вызвать [**ID3D12Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) , чтобы запросить экстент, в котором драйвер устройства и/или оборудование эффективно поддерживают проходы отрисовки.

```cppwinrt
D3D12_RENDER_PASS_TIER get_render_passes_tier(::ID3D12Device * pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS5 featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS5, &featureSupport, sizeof(featureSupport))
    );
    return featureSupport.RenderPassesTier;
}
...
    D3D12_RENDER_PASS_TIER renderPassesTier{ get_render_passes_tier(pIDevice) };
```

Из-за логики сопоставления среды выполнения функция Render передает значение Always. Но в зависимости от поддержки функций они не всегда предоставляют преимущество. Вы можете использовать код, похожий на приведенный выше пример кода, чтобы определить, стоит ли время выполнять команды в процессе подготовки к просмотру, и когда она определенно не является преимуществом (т. е. когда среда выполнения просто сопоставляется с существующей поверхностью API). Выполнение этой проверки особенно важно, если вы используете [D3D11On12](/windows/desktop/direct3d12/direct3d-11-on-12)).

Описание трех уровней поддержки см. в разделе Перечисление [**D3D12_RENDER_PASS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier) .
