---
title: Вопросы и ответы по Direct3D 10
description: Эта статья содержит некоторые часто задаваемые вопросы, связанные с Direct3D 10, от точки зрения разработчика, который переносит существующее приложение с Direct3D 9 (D3D9) на Direct3D 10 (D3D10).
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134131"
---
# <a name="direct3d-10-frequently-asked-questions"></a>Вопросы и ответы по Direct3D 10

Эта статья содержит некоторые часто задаваемые вопросы, связанные с Direct3D 10, от точки зрения разработчика, который переносит существующее приложение с Direct3D 9 (D3D9) на Direct3D 10 (D3D10).

-   [Буферы констант](#constant-buffers)
-   [Состояние](#state)
-   [Форматы](#formats)
-   [Компоновка шейдера](#shader-linkage)
-   [Вызовы Draw](#draw-calls)
-   [Ресурсы](#resources)
-   [Глубина как текстура](#depth-as-texture)
-   [MSAA](#msaa)
-   [Сбои](#crashes)
-   [Отрисовка с предикатом](#predicated-rendering)
-   [Шейдер геометрии](#geometry-shader)
-   [HLSL](#hlsl)

## <a name="constant-buffers"></a>Буферы констант

<dl> <dt>

<span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>Как лучше всего обновлять буферы констант?
</dt> <dd>

Упдатесубресаурце и Map с отклонениями должны иметь одинаковую скорость. Выберите один из них в зависимости от того, какой из них копирует минимальный объем памяти. Если данные, хранящиеся в памяти, уже хранятся в одном непрерывном блоке, используйте Упдатесубресаурце. Если необходимо накапливать данные из других мест, используйте Map с параметром Discard.

</dd> <dt>

<span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>Каков самый худший способ организации буферов констант?
</dt> <dd>

Наихудшая производительность достигается путем помещения всех констант для конкретного шейдера в один буфер констант. Хотя это и часто является самым простым способом переноса с D3D9 на D3D10, он может криппле производительность. Например, рассмотрим ситуацию, в которой используется следующий буфер констант:

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

Буфер равен 6560 байт. Предположим, что имеется приложение с 1000 объектами для подготовки к просмотру, 100 из которых представляют собой сетчатые сети, а 900 — статические сетки. Кроме того, предположим, что это приложение использует теневое сопоставление с одним источником освещения. Это означает, что существует два прохода: один для карты глубины, отображаемый на свете, и один для прохода прямой отрисовки. Это приводит к 2000 вызовов Draw. Хотя каждому вызову Draw не требуется обновлять все части буфера констант, весь буфер констант по-прежнему обновляется и отправляется на карту. Это приводит к обновлению 13 МБ данных в каждом кадре (2000 вызовов времени вызова 6560 КБ).

</dd> <dt>

<span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>Каков лучший способ организации постоянных буферов?
</dt> <dd>

Лучший способ — упорядочить постоянные буферы по частоте обновления. Константы, которые обновляются с одинаковыми частотой, должны находиться в одном буфере. Например, рассмотрим сценарий, представленный в разделе "что является наихудшим способом организации буферов констант?", но с более подходящим макетом постоянной структуры:

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

Буферы констант разбиваются по частоте обновления, но это лишь половина решения. Приложению необходимо правильно обновить буферы констант, чтобы воспользоваться всеми преимуществами разбиения. Мы будем рассчитывать на ту же сцену, что и на примере выше: 900. статические сетки, 100 в обложках, один проход и один проход вперед. Также предполагается, что будут храниться некоторые константные буферы на объект. Это означает, что каждый объект будет содержать либо Всперскиннедкб, либо Всперстатиккб в зависимости от того, является ли он обложкой или статичным. Мы делаем это, чтобы избежать удвоения количества матриц, отправленных по конвейеру.

Мы разбиваем фрейм на три фазы. Первый этап является началом кадра и не включает отрисовку, а только постоянные обновления.

<dl> <dt>

<span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Начальный кадр**
</dt> <dd>

-   Обновление Всглобалперфрамекб для времени приложения (4 байта)
-   Обновление 100 Всперскиннедкб для объектов с обложкой 100 (640000 байт)
-   Обновление Всперстатиккб для 900 статических объектов (57600 байт)

Далее следует проход теневой карты. Обратите внимание, что фактически обновляются только постоянные буферы Всперпасскб. Все остальные буферы констант были обновлены во время прохода начала кадра. Хотя нам все равно нужно привязывать эти буферы констант, объем данных, передаваемых видеоадаптеру, минимальен, поскольку буферы уже обновлены.

</dd> <dt>

<span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Проход тени**
</dt> <dd>

-   Обновление Всперпасскб (72 байт)
-   Рисование 100 сеток с обложками (100, привязки, без обновлений)
-   Рисование 900 статических сеток (100 привязок, без обновлений)

Аналогичным образом, проход прямой визуализации должен обновить данные для каждого материала, так как он не хранился отдельно для каждой сети. Если предполагается, что в сцене используется 500 материалов:

</dd> <dt>

<span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Прямой проход**
</dt> <dd>

-   Обновление Всперпасскб (72 байт)
-   Обновление 500 Всперматериалкбс (10000 байт)

Это приводит к общему объему всего 707 КБ. Хотя это очень надуманный сценарий, он показывает, сколько постоянных затрат на обновление можно уменьшить, сортируя константы по частоте обновления.

</dd> </dl> </dd> <dt>

<span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>Что делать, если у меня недостаточно места для хранения отдельных буферов констант для моих сеток, материалов и т. д.? 
</dt> <dd>

Вы всегда можете использовать многоуровневые системы буферов констант. Создайте буферы констант с переменным размером (16 байт, 32 байт, 64 байт и т. д.) вплоть до самого большого необходимого размера буфера константы. Когда необходимо привязать буфер константы к шейдеру, выберите наименьший буфер констант, который может содержать данные, необходимые шейдеру. Хотя этот подход немного менее эффективен, это хороший промежуточный шаг.

</dd> <dt>

<span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Я использую постоянные буферы между разными шейдерами. Один шейдер может использовать все константы, но другой может использовать некоторые константы. Как лучше всего обновлять эти данные? 
</dt> <dd>

Один из подходов состоит в том, чтобы разделить буфер констант еще дальше. Однако имеется точка, в которой привязано слишком много буферов констант. В этом случае переместите константы, которые, скорее всего, не будут использоваться несколькими шейдерами, в конец буфера констант. При получении данных переменной из шейдера используйте \_ флаг D3D10 SVF \_ из \_ переменной D3D10 шейдера \_ DESC, \_ чтобы определить, используется ли переменная. Поместив неиспользуемые переменные в конец буфера констант, можно привязать меньший буфер к шейдеру, который не использует эти переменные, тем самым сохраняя стоимость обновления.

</dd> <dt>

<span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>Сколько я могу улучшить свою частоту кадров, если только я загрузил кости моего знака один раз для каждого кадра, а не один раз для каждого прохода или рисования? 
</dt> <dd>

Можно увеличить частоту кадров в диапазоне от 8 до 50 процентов в зависимости от объема избыточных данных. В худшем случае производительность не будет снижена.

</dd> <dt>

<span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>Сколько буферов констант следует привязать сразу? 
</dt> <dd>

Привяжите минимальное число буферов констант, необходимое для получения всех данных в шейдер. В реалистичном сценарии для использования рекомендуется использовать пять буферов констант. Предоставление общего доступа к постоянным буферам между шейдерами (привязка одного и того же CB к VS и PS) также может повысить производительность.

</dd> <dt>

<span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Существуют ли затраты на связывание буферов констант без их использования? 
</dt> <dd>

Да, если вы не собираетесь использовать буфер, не вызывайте Вссетконсантбуффер или Пссетконстантбуффер. Эти дополнительные издержки на API могут сложиться в рамках нескольких вызовов Draw.

</dd> </dl>

## <a name="state"></a>Состояние

<dl> <dt>

<span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>Каков лучший способ управления состоянием в D3D10? 
</dt> <dd>

Лучшим решением является знание всех состояний на передний план и создание объектов состояния на передний план. Это означает, что во время визуализации привязка состояния является единственной операцией, которая должна быть выполнена. D3D10 также отфильтровывает дубликаты.

</dd> <dt>

<span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Моя игра загружена динамически или содержит содержимое, созданное пользователем. Не удается загрузить все объекты состояния впереди.   Что следует делать? 
</dt> <dd>

Здесь есть два решения. Первый — просто создать объекты состояния на лету и позволить D3D10 отфильтровать дубликаты. Однако это не рекомендуется для сценариев с множеством изменений объектов состояния на кадр. Лучшее решение заключается в том, чтобы вручную хэшировать объекты состояния и создавать объекты состояния, только если в хэш-таблице не найден соответствующий требованиям. Причиной использования пользовательской хэш-таблицы является то, что приложение может выбрать быстрый хэш на основе сценария использования, определенного для этого приложения. Например, если приложение изменяет только рендертаржетвритемаск в Блендстате и сохраняет все остальные значения, приложение может создать хэш из рендертаржетвритемаск, а не всю структуру.

</dd> <dt>

<span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>Состояние Алфатест. Куда она пойдет? 
</dt> <dd>

Алфатест теперь должен быть производительностью шейдера. См. пример Фикседфунцему.

</dd> <dt>

<span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>Что случилось с пользовательскими роликами? 
</dt> <dd>

Ролики пользователя были перемещены в шейдер. Это можно решить двумя способами. Первый — вывод SV \_ клипдистанце из шейдера вершин или шейдера Geometry. Другой вариант — использовать параметр «отбросить» в шейдере пикселей в зависимости от значения, переданного с помощью шейдера вершин или шейдера Geometry. Поэкспериментируйте с обоими, чтобы узнать, какой из них быстрее в вашем конкретном сценарии. Использование SV \_ клипдистанце может привести к тому, что оборудование будет использовать подпрограмму отсечения, основанную на геометрии, которая может привести к более медленному запуску вызовов рисования геометрических границ. Аналогично, использование функции «отмена» сдвигает работу на шейдер пикселей, что может привести к более медленному выполнению вызовов рисования, привязанных к пикселю.

</dd> <dt>

<span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Снятые флажки не учитывают параметры состояния, такие как параметры прямоугольного Rect в своем состоянии средства программной прорисовки. 
</dt> <dd>

Очистки были отделены от состояния конвейера. Чтобы получить поведение в стиле D3D9, нужно эмулировать очистку, выполняя четыре экрана.

</dd> <dt>

<span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Я установил для моих состояний значение по умолчанию, чтобы попробовать и диагностировать ошибку отрисовки. Теперь на экране отображается черный цвет, хотя я могу понять, что на экране рисуются объекты. 
</dt> <dd>

При установке состояния обратно в значения по умолчанию (NULL) убедитесь, что Самплемаск в вызове Омсетблендстате никогда не равен нулю. Если Самплемаск имеет значение 0, то все примеры логически и с нулевым значением. В этом случае ни один из примеров не будет проходить тест Blend.

</dd> <dt>

<span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Куда D3DSAMP \_ состояние сргбтекстуреа? 
</dt> <dd>

SRGB был удален как часть состояния образца и теперь привязан к формату текстуры. Привязка текстуры SRGB приведет к той же выборки, которая будет возникать, если вы указали D3DSAMP \_ сргбтекстуре в Direct3D 9.

</dd> </dl>

## <a name="formats"></a>Форматы

<dl> <dt>

<span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Какой формат D3D9 соответствует формату D3D10? 
</dt> <dd>

Дополнительные сведения см. [в статье требования Direct3D 9 к Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

</dd> <dt>

<span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>Что случилось с форматами текстур A8R8G8B8? 
</dt> <dd>

Они являются устаревшими в D3D10. Вы можете повторно источникировать текстуры как R8G8B8A8 или свиззле по нагрузке или свиззле в шейдере.

</dd> <dt>

<span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>Разделы справки использовать текстуры палеттизед? 
</dt> <dd>

Поместите цветовую палитру в текстуру или буфер констант и привяжите ее к конвейеру. В шейдере пикселей выполните косвенный Просмотр с помощью индекса в текстуре палеттизед.

</dd> <dt>

<span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>Что такое новые форматы SRGB? 
</dt> <dd>

SRGB был удален как часть состояния образца и теперь привязан к формату текстуры. Привязка текстуры SRGB приведет к той же выборки, которая будет возникать, если вы указали D3DSAMP \_ сргбтекстуре в Direct3D 9.

</dd> <dt>

<span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Где находятся вентиляторы треугольника? 
</dt> <dd>

Треугольные вентиляторы не рекомендуются в D3D10. Вентиляторы треугольника необходимо преобразовать в конвейер содержимого или при загрузке.

</dd> </dl>

## <a name="shader-linkage"></a>Компоновка шейдера

<dl> <dt>

<span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Мои шейдеры Direct3D 9 прекрасно компилируются в модель шейдера 4,0, но, когда я привязал их к конвейеру, я получаю ошибки компоновки, которые отображаются в отладочном выводе с помощью отладочной среды выполнения. 
</dt> <dd>

Компоновка шейдера является намного более строгой в D3D10. Элементы на следующем этапе должны считываться в том порядке, в котором они выводятся на предыдущем этапе. Пример:

Выходные данные шейдера вершин:

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

Построитель текстуры считывает в:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

Хотя в шейдере пикселей это не требуется, это вызовет ошибку компоновки, так как расположение выводится из шейдера вершин, но не считывается шейдером пикселей. Более правильная версия будет выглядеть следующим образом:

Выходные данные шейдера вершин:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

Построитель текстуры считывает в:

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

В этом случае шейдер вершин выводит одну и ту же информацию, но теперь шейдер пикселей считывает элементы в выходных данных заказа. Поскольку построитель текстуры не читается что-то после Да, нам не нужно беспокоиться о том, чтобы в VS выводиться больше информации, чем при считывании PS.

</dd> <dt>

<span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>Для создания макета ввода требуется подпись шейдера, но перед созданием шейдеров необходимо загрузить сетки и создать макеты. Что делать? 
</dt> <dd>

Одним из решений является переключение параметров Order и Load перед загрузкой сеток. Однако это гораздо проще сказать, чем это сделано. Вы всегда можете создать входные макеты по запросу, если это необходимо для приложения. Вам потребуется использовать версию сигнатуры шейдера. Необходимо создать хэш, основанный на шейдере и макете буфера, и создать только входной макет, если тот, который соответствует, еще не существует.

</dd> </dl>

## <a name="draw-calls"></a>Вызовы Draw

<dl> <dt>

<span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>Каково ограничение на вызовы Draw для D3D10 до 60 Гц? 30 Гц? 
</dt> <dd>

Direct3D 9 имел ограничение на количество вызовов Draw из-за стоимости ЦП на вызов Draw. В Direct3D 10 стоимость каждого вызова Draw уменьшилась. Однако больше не существует определенной корреляции между вызовами рисования и частотой кадров. Поскольку вызовы Draw часто потребовали много обращений в службу поддержки (обновления буфера констант, привязки текстур, настройки состояния и т. д.), воздействие частоты кадров API теперь более зависит от общего использования API, а не просто выводит число вызовов.

</dd> </dl>

## <a name="resources"></a>Ресурсы

<dl> <dt>

<span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>Какой тип использования ресурсов следует использовать для каких операций? 
</dt> <dd>

Используйте следующий Памятка по-лист:

-   ЦП обновляет ресурс более одного раза в кадре: D3D10 \_ использование \_ dynamic.
-   ЦП обновляет ресурс менее одного раза в кадре: D3D10 \_ использование \_ по умолчанию
-   ЦП не обновляет ресурс: D3D10 \_ Usage \_ неизменяемый
-   ЦП должен прочитать ресурс: D3D10 \_ использование \_ промежуточного хранения

Так как постоянные буферы всегда предназначены для регулярного обновления, они не соответствуют "Памятка по-Sheet". Сведения о типах ресурсов, используемых для буферов констант, см. в разделе [постоянные буферы](#constant-buffers) .

</dd> <dt>

<span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>Что случилось с Дравпримитивеуп и Дравиндекседпримитивеуп? 
</dt> <dd>

Они исчезают в D3D10. Для динамической геометрии используйте динамический буфер D3D10 большого объема \_ использования \_ . В начале кадра сопоставьте его с D3D10ной \_ \_ записью \_ отказа в карте. Для каждого последующего вызова Draw измените указатель записи после позиции ранее рисуемых вершин и сопоставьте буфер с D3D10 \_ Map \_ \_ не \_ перезаписывает. Если ближе к концу буфера перед концом кадра, заключите указатель записи в начало и карту с D3D10ом \_ записи в Map \_ \_ .

</dd> <dt>

<span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Можно ли записывать 16-битные индексы и 32-битовые индексы в один и тот же динамический буфер Geometry? 
</dt> <dd>

Да, можно, но это может привести к снижению производительности на определенном оборудовании. Можно более безопасно создавать отдельные буферы для динамических 16-битных данных индекса и 32-битных индексных данных.

</dd> <dt>

<span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Разделы справки считать данные из GPU в ЦП? 
</dt> <dd>

Необходимо использовать промежуточный ресурс. Скопируйте данные из ресурса GPU в промежуточный ресурс с помощью Копиресаурце. Сопоставьте промежуточный ресурс для чтения данных.

</dd> <dt>

<span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>Приложение было зависело от функциональных возможностей Стретчрект. 
</dt> <dd>

Поскольку это является, по сути, оболочкой для базовых функций Direct3D, она была удалена из API. Некоторые функции Стретчрект были перемещены в D3DX10LoadTextureFromTexture. Для преобразований формата и копирования текстур D3DX10LoadTextureFromTexture может выполнить задание. Однако операции, такие как преобразование из одного размера в другой, скорее всего, потребует выполнения операции рендеринга для текстуры в приложении.

</dd> <dt>

<span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>Нет смещений или размеров для вызовов карт для ресурсов. Это было вызвано вызовами блокировок на Direct3D 9; Почему они изменились? 
</dt> <dd>

Смещения и размеры вызовов блокировок в Direct3D 9, по сути, были перегружены API и часто игнорируются драйвером. Смещение должно рассчитываться приложением из указателя, возвращенного в вызове Map.

</dd> </dl>

## <a name="depth-as-texture"></a>Глубина как текстура

<dl> <dt>

<span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Что быстрее? Как использовать глубину в качестве текстуры или глубины записи в альфа-канал и считывать их? 
</dt> <dd>

Это зависит от приложения и оборудования. Используйте любой из них, чтобы сохранить наибольшую пропускную способность. Если вы уже используете несколько целевых объектов рендеринга и у вас есть дополнительный канал, то более эффективным решением может стать запись глубины из шейдера. Кроме того, запись глубины в альфа или другой целевой объект прорисовки позволяет создавать линейные значения глубины, которые могут ускорить вычисления, которым требуется доступ к буферу глубины.

</dd> <dt>

<span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Можно ли привязать текстуру в качестве входных данных и привязать ее как текстуру трафарета глубины, если отключить запись глубины? 
</dt> <dd>

Не в D3D10.

</dd> </dl>

## <a name="msaa"></a>MSAA

<dl> <dt>

<span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Можно ли разрешить текстуру набора элементов в MSAA с глубиной? 
</dt> <dd>

Не в D3D10. Однако можно выполнить выборку отдельных образцов из текстуры MSAA. Дополнительные сведения см. в разделе [HLSL](#hlsl) .

</dd> <dt>

<span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Почему происходит сбой моего приложения сразу после включения MSAA? 
</dt> <dd>

Убедитесь, что вы включаете число образцов MSAA и номер качества, которые фактически перечисляются драйвером.

</dd> </dl>

## <a name="crashes"></a>Сбои

<dl> <dt>

<span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>Мое приложение аварийно завершает работу в D3D10 или в драйвере, и я не знал, почему. 
</dt> <dd>

Первым шагом является включение среды выполнения отладки ([**D3D10 \_ CREATE Device флаг \_ \_ отладки**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) , переданный в [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). Это позволит вывести наиболее распространенные ошибки как выходные данные отладки.

</dd> <dt>

<span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX аварийно завершает работу при попытке использовать приложение с ним. 
</dt> <dd>

Первым шагом является включение среды выполнения отладки ([**D3D10 \_ CREATE Device флаг \_ \_ отладки**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) , переданный в [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). В случае неочистки выходных данных отладки PIX имеет более высокую вероятность сбоя.

</dd> <dt>

<span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Моя игра заканчивается виртуальным адресным пространством в 32-разрядной версии Vista в D3D10. У него нет проблем с D3D9. 
</dt> <dd>

Возникли проблемы с D3D10 и виртуальным адресным пространством. Это было исправлено в [KB940105](https://support.microsoft.com/kb/940105). Если это не устраняет проблему, убедитесь, что вы не создаете больше ресурсов, которые могут быть сопоставлены (заблокированы) в D3D10, чем при создании в D3D9. Также Подумайте о переносе в 64-бит, так как это станет более распространенным в будущем.

</dd> </dl>

## <a name="predicated-rendering"></a>Отрисовка с предикатом

<dl> <dt>

<span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>Я использовал отработку по предикату (на основе результатов запроса перекрытия). Почему мое приложение по-прежнему имеет одинаковую скорость? 
</dt> <dd>

Во-первых, убедитесь, что визуализация, которую нужно пропустить, на самом деле является узким местом приложения. Если это не узкое место, то пропуск отрисовки не поможет оценить частоту кадров.

Во вторых, убедитесь в том, что между выпуском запроса и отрисовкой, которую вы хотите отдать предикату, достаточно времени. Если запрос не завершен до тех пор, пока вызов прорисовки не достигнет графического процессора, отрисовка будет выполняться в любом случае.

В третьих, затенения пропускает только определенные вызовы. Пропущенные вызовы — это прорисовка, очистка, копирование, обновление, Ресолвесубресаурце и Женератемипс. Параметры состояния, установки IA, Map и CREATE не учитывают затенения. При наличии большого количества вызовов параметра State для предиката Draw все равно будут заданы эти состояния.

</dd> </dl>

## <a name="geometry-shader"></a>Шейдер геометрии

<dl> <dt>

<span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Следует ли использовать шейдер Geometry для тесселяции My (вставить здесь все)? 
</dt> <dd>

Нет. Шейдер геометрии не следует использовать для тесселяции.

</dd> <dt>

<span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Можно ли использовать шейдер геометрии для создания геометрии? 
</dt> <dd>

Да, в очень ограниченных сценариях. Шейдер геометрии в текущих частях D3D10 (2008) не может справиться с большим расширением. Это может измениться в будущем. Производители видеоадаптеров могут иметь специальный путь для одного и четырех расширений из-за имеющегося оборудования для работы с точками спрайта. Любое другое расширение должно быть очень ограниченным. Примеры Партиклесгс и Пипесгс обеспечивают высокую частоту кадров, выполняя только ограниченное расширение. Для каждого кадра разворачивается всего несколько точек.

</dd> <dt>

<span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>Для чего следует использовать шейдер геометрии? 
</dt> <dd>

Все, что требует операций над целым примитивом, таким как обнаружение силуэт, координаты барицентрик и т. д. Также используйте его для выбора среза целевого массива прорисовки для отправки примитивов.

</dd> <dt>

<span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Можно ли выводить переменные объемов геометрии из шейдера Geometry? 
</dt> <dd>

Да, но это может вызвать проблемы с производительностью. Возьмем пример вывода 1 точки для одного вызова и 4 точек для другого. При соблюдении правил расширения это может привести к последовательному выполнению потоков шейдеров Geometry.

</dd> <dt>

<span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>Как D3D10 знает, как создавать смежные индексы для моей сетки? Или, почему D3D10 не отображается правильно при указании того, что шейдеру Geometry требуются сведения о смежности. 
</dt> <dd>

Сведения о соседических данных не создаются D3D10, а приложением. Смежные индексы создаются приложением и должны содержать шесть индексов для каждого примитива; из шести нечетных пронумерованных индексов расположены граничные смежные вершины. Для создания этих данных можно использовать ID3DX10Mesh:: Женератеаджаценциандпоинтсрепс.

</dd> </dl>

## <a name="hlsl"></a>HLSL

<dl> <dt>

<span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Являются ли целочисленные и побитовые инструкции замедляются? 
</dt> <dd>

Они могут быть. Различные карты D3D10 могут быть способны выдавать целочисленные операции только для подмножества доступных единиц ALU. Это сильно зависит от оборудования. Рекомендации по устранению целочисленных операций на этом конкретном оборудовании см. в отдельном поставщике оборудования. Кроме того, будьте внимательны при приведении типов.

</dd> <dt>

<span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>Что случилось с ВПОС? 
</dt> <dd>

Если вы объявили входные данные для шейдера пикселей как значение ОКП \_ , вы получите то же поведение, что и объявление его как впос.

</dd> <dt>

<span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Разделы справки пример текстуры MSAA? 
</dt> <dd>

В шейдере объявите текстуру как Texture2DMS. Затем можно получить отдельные образцы, используя примеры методов из объекта Texture2DMS.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Разделы справки определить, действительно ли используется переменная шейдера в буфере константы? 
</dt> <dd>

Взгляните на отраженную \_ переменную D3D10 шейдера \_ \_ DESC struct для этой переменной. для Уфлагс должен быть \_ \_ установлен флаг D3D10 SVF.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Разделы справки определить, использует ли переменная шейдера в буфере константы FX10? 
</dt> <dd>

В настоящее время это невозможно сделать с помощью FX10.

</dd> <dt>

<span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>У меня нет возможности управлять константными буферами, создаваемыми FX10. Как они создаются и обновляются? 
</dt> <dd>

Все управляемые FX10 буферы констант создаются как \_ \_ ресурсы по умолчанию для D3D10 использования и обновляются с помощью упдатесубресаурце. Так как FX10 сохраняет резервное хранилище всех постоянных данных, Упдатесубресаурце является лучшим подходом к их обновлению.

</dd> <dt>

<span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Разделы справки эмулировать фиксированный конвейер функций с помощью шейдеров? 
</dt> <dd>

См. пример Фикседфунцему.

</dd> <dt>

<span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Следует ли использовать новую \[ \] \[ подсказку компилятора (unroll, цикл \] , \[ ветвь \] и т. д.)? 
</dt> <dd>

Как правило, нет. Компилятор часто пытается воспользоваться обоими способами и выбирает самый быстрый из них. В некоторых случаях может потребоваться использовать \[ unroll \] , например, когда выбор текстуры в цикле требует доступа к градиенту.

</dd> <dt>

<span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Отличается ли частичная точность от D3D10? Я могу указать частичную точность в моем D3D9 HLSL, но не в D3D10 HLSL. 
</dt> <dd>

Все операции D3D10 заданы для выполнения с точностью до 32 бит с плавающей точкой. Поэтому частичная точность не должна делать никаких различий в D3D10.

</dd> <dt>

<span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>В D3D9 я могу выполнить HW PCF Shadow Filtering, привязывая буфер глубины в качестве текстуры и используя регулярные инструкции tex2d HLSL. Разделы справки сделать это в D3D10? 
</dt> <dd>

Необходимо использовать состояние образца сравнения и использовать инструкции Самплекмп.

</dd> <dt>

<span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>Как это ключевое слово Register работает в D3D10? 
</dt> <dd>

Ключевое слово Register в D3D10 теперь применяется к области, к которой привязан конкретный ресурс. В этом случае ресурсом может быть буфер (константа или иным образом), текстура или образец.

-   Для буферов констант используйте синтаксис: Register (млрд долл), где N — входной слот (0-15)
-   Для текстур используйте синтаксис: Register (тн), где N — входной слот (0-127).
-   Для пробов используйте синтаксис: Register (sN), где N — входной слот (0-127)

</dd> <dt>

<span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Разделы справки поместить переменную в буфер константы, если регистр используется только для указания места привязки всего буфера? 
</dt> <dd>

Используйте ключевое слово паккоффсет. Аргумент для паккоффсет имеет формат c \[ 0-4095 \] . \[ x, y, z, w \] . Пример:

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

В этом буфере констант IWaste2Floats помещается в третий массив с плавающей запятой (12-й байт) в буфер констант. Ивастеморе помещается в 13-й float4 или 52nd float в буфере констант.

</dd> </dl>

 

 