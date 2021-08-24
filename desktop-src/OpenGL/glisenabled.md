---
title: Функция Глисенаблед (GL. h)
description: Функция Гллсенаблед проверяет, включена ли возможность.
ms.assetid: 18df5a6f-dc21-434d-a2e8-2c58597df037
keywords:
- Функция Глисенаблед OpenGL
topic_type:
- apiref
api_name:
- glIsEnabled
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3237cedc1daeffa3fd47fd50b9b19d79ebad3acbf53bdd7929b70dad4093a7a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493404"
---
# <a name="glisenabled-function"></a>Функция Глисенаблед

Функция **гллсенаблед** проверяет, включена ли возможность.

## <a name="syntax"></a>Синтаксис


```C++
GLboolean WINAPI glIsEnabled(
   GLenum cap
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*заполнен* 
</dt> <dd>

Символьная константа, указывающая на возможность OpenGL. Принимаются следующие возможности.



| Значение                                                                                                                                                                                                    | Значение                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span><dl> <dt>**\_альфа- \_ тест GL**</dt> </dl>                                           | См. [ **глалфафунк**](glalphafunc.md)<br/>                                                                                                   |
| <span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span><dl> <dt>**Автоматический режим "GL" \_ \_**</dt> </dl>                                        | См. [ **глевалкурд**](glevalcoord-functions.md)<br/>                                                                                         |
| <span id="GL_BLEND"></span><span id="gl_blend"></span><dl> <dt>**ГК \_ Blend**</dt> </dl>                                                           | См. [ **глблендфунк**](glblendfunc.md)<br/>                                                                                                   |
| <span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span><dl> <dt>* * \_ Плоскость для вырезов * * * * * * * * * * * \_</dt> </dl> | См. [ **глклипплане**](glclipplane.md)<br/>                                                                                                   |
| <span id="GL_COLOR_ARRAY"></span><span id="gl_color_array"></span><dl> <dt>**\_массив цветов \_ GL**</dt> </dl>                                        | См. [ **глколорпоинтер**](glcolorpointer.md)<br/>                                                                                             |
| <span id="GL_COLOR_LOGIC_OP"></span><span id="gl_color_logic_op"></span><dl> <dt>**\_ \_ Операция логики цвета GL \_**</dt> </dl>                              | См. [ **гллогикоп**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span><dl> <dt>**\_цветовой \_ материал GL**</dt> </dl>                               | См. [ **глколорматериал**](glcolormaterial.md)<br/>                                                                                           |
| <span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span><dl> <dt>**\_лицо для отбора GL \_**</dt> </dl>                                              | См. [ **глкуллфаце**](glcullface.md)<br/>                                                                                                     |
| <span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span><dl> <dt>**\_тест глубины \_ GL**</dt> </dl>                                           | См. раздел [**глдепсфунк**](gldepthfunc.md) and [**глдепсранже**](gldepthrange.md)<br/>                                                          |
| <span id="GL_DITHER"></span><span id="gl_dither"></span><dl> <dt>**\_ДИЗЕРИНГ GL**</dt> </dl>                                                        | См. [ **гленабле**](glenable.md)<br/>                                                                                                         |
| <span id="GL_FOG"></span><span id="gl_fog"></span><dl> <dt>**\_туман GL**</dt> </dl>                                                                 | См. [ **глфог**](glfog.md)<br/>                                                                                                               |
| <span id="GL_INDEX_ARRAY"></span><span id="gl_index_array"></span><dl> <dt>**\_массив индексов GL \_**</dt> </dl>                                        | См. [ **глиндекспоинтер**](glindexpointer.md)<br/>                                                                                             |
| <span id="GL_INDEX_LOGIC_OP"></span><span id="gl_index_logic_op"></span><dl> <dt>**\_ \_ Операция логики индекса GL \_**</dt> </dl>                              | См. [ **гллогикоп**](gllogicop.md)<br/>                                                                                                       |
| <span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span><dl> <dt>* * GL- \_ светло * i * * *</dt> </dl>                      | См. раздел [**гллигхтмодел**](gllightmodel-functions.md) and [**гллигхт**](gllight-functions.md)<br/>                                              |
| <span id="GL_LIGHTING"></span><span id="gl_lighting"></span><dl> <dt>**освещение в ГК \_**</dt> </dl>                                                  | См. раздел [**глматериал**](glmaterial-functions.md), [**гллигхтмодел**](gllightmodel-functions.md)и [**гллигхт**](gllight-functions.md)<br/> |
| <span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span><dl> <dt>**\_ \_ сглаженная линия GL**</dt> </dl>                                        | См. [ **гллиневидс**](gllinewidth.md)<br/>                                                                                                   |
| <span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span><dl> <dt>**\_стиппле строки \_ GL**</dt> </dl>                                     | См. [ **гллинестиппле**](gllinestipple.md)<br/>                                                                                               |
| <span id="GL_MAP1_COLOR_4"></span><span id="gl_map1_color_4"></span><dl> <dt>**«Карта1» GL, \_ \_ Цвет \_ 4**</dt> </dl>                                    | См. [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_INDEX"></span><span id="gl_map1_index"></span><dl> <dt>**\_Индекс «КАРТА1» \_ GL**</dt> </dl>                                           | См. [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_NORMAL"></span><span id="gl_map1_normal"></span><dl> <dt>**«Карта1» GL ( \_ \_ Обычная)**</dt> </dl>                                        | См. [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_1"></span><span id="gl_map1_texture_coord_1"></span><dl> <dt>**\_«Карта1» \_ текстура GL \_ курд \_ 1**</dt> </dl>           | См. [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_2"></span><span id="gl_map1_texture_coord_2"></span><dl> <dt>**GL \_ «Карта1» \_ текстура \_ курд \_ 2**</dt> </dl>           | См. [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_3"></span><span id="gl_map1_texture_coord_3"></span><dl> <dt>**\_«Карта1» \_ текстура GL \_ курд \_ 3**</dt> </dl>           | См. [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_TEXTURE_COORD_4"></span><span id="gl_map1_texture_coord_4"></span><dl> <dt>**\_«Карта1» \_ текстура GL \_ курд \_ 4**</dt> </dl>           | См. [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_3"></span><span id="gl_map1_vertex_3"></span><dl> <dt>**GL \_ «Карта1», \_ вершина \_ 3**</dt> </dl>                                 | См. [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP1_VERTEX_4"></span><span id="gl_map1_vertex_4"></span><dl> <dt>**\_«Карта1»ная \_ вершина GL \_ 4**</dt> </dl>                                 | См. [ **glMap1**](glmap1.md)<br/>                                                                                                             |
| <span id="GL_MAP2_COLOR_4"></span><span id="gl_map2_color_4"></span><dl> <dt>**MAP2 GL, \_ \_ Цвет \_ 4**</dt> </dl>                                    | См. [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_INDEX"></span><span id="gl_map2_index"></span><dl> <dt>**\_Индекс MAP2 \_ GL**</dt> </dl>                                           | См. [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_NORMAL"></span><span id="gl_map2_normal"></span><dl> <dt>**MAP2 GL ( \_ \_ Обычная)**</dt> </dl>                                        | См. [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_1"></span><span id="gl_map2_texture_coord_1"></span><dl> <dt>**\_MAP2 \_ текстура GL \_ курд \_ 1**</dt> </dl>           | См. [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_2"></span><span id="gl_map2_texture_coord_2"></span><dl> <dt>**GL \_ MAP2 \_ текстура \_ курд \_ 2**</dt> </dl>           | См. [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_3"></span><span id="gl_map2_texture_coord_3"></span><dl> <dt>**\_MAP2 \_ текстура GL \_ курд \_ 3**</dt> </dl>           | См. [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_TEXTURE_COORD_4"></span><span id="gl_map2_texture_coord_4"></span><dl> <dt>**\_MAP2 \_ текстура GL \_ курд \_ 4**</dt> </dl>           | См. [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_3"></span><span id="gl_map2_vertex_3"></span><dl> <dt>**GL \_ map2, \_ вершина \_ 3**</dt> </dl>                                 | См. [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_MAP2_VERTEX_4"></span><span id="gl_map2_vertex_4"></span><dl> <dt>**\_MAP2ная \_ вершина GL \_ 4**</dt> </dl>                                 | См. [ **glMap2**](glmap2.md)<br/>                                                                                                             |
| <span id="GL_NORMAL_ARRAY"></span><span id="gl_normal_array"></span><dl> <dt>**\_стандартный \_ массив GL**</dt> </dl>                                     | См. [ **глнормалпоинтер**](glnormalpointer.md)<br/>                                                                                           |
| <span id="GL_NORMALIZE"></span><span id="gl_normalize"></span><dl> <dt>**\_нормализация GL**</dt> </dl>                                               | См. [ **глнормал**](glnormal-functions.md)<br/>                                                                                               |
| <span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span><dl> <dt>**\_ \_ гладкий пункт GL**</dt> </dl>                                     | См. [ **глпоинтсизе**](glpointsize.md)<br/>                                                                                                   |
| <span id="GL_POLYGON_OFFSET_FILL"></span><span id="gl_polygon_offset_fill"></span><dl> <dt>**\_ \_ Заливка смещения МНОГОУГОЛЬНИКа GL \_**</dt> </dl>               | См. [ **глполигоноффсет**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_LINE"></span><span id="gl_polygon_offset_line"></span><dl> <dt>**\_строка смещения многоугольника GL \_ \_**</dt> </dl>               | См. [ **глполигоноффсет**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_OFFSET_POINT"></span><span id="gl_polygon_offset_point"></span><dl> <dt>**\_точка смещения многоугольника GL \_ \_**</dt> </dl>            | См. [ **глполигоноффсет**](glpolygonoffset.md)<br/>                                                                                           |
| <span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span><dl> <dt>**\_несглаженный МНОГОУГОЛЬНИК GL \_**</dt> </dl>                               | См. [ **глполигонмоде**](glpolygonmode.md)<br/>                                                                                               |
| <span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span><dl> <dt>**\_стиппле многоугольника GL \_**</dt> </dl>                            | См. [ **глполигонстиппле**](glpolygonstipple.md)<br/>                                                                                         |
| <span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span><dl> <dt>**\_тест вырезание GL \_**</dt> </dl>                                     | См. [ **глсЦиссор**](glscissor.md)<br/>                                                                                                       |
| <span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span><dl> <dt>**\_тест шаблона \_ GL**</dt> </dl>                                     | См. раздел [**глстенЦилфунк**](glstencilfunc.md) and [**глстенЦилоп**](glstencilop.md)<br/>                                                        |
| <span id="GL_TEXTURE_1D"></span><span id="gl_texture_1d"></span><dl> <dt>**\_Одномерное текстура GL \_**</dt> </dl>                                           | См. [ **glTexImage1D**](glteximage1d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_2D"></span><span id="gl_texture_2d"></span><dl> <dt>**\_2D-текстура GL \_**</dt> </dl>                                           | См. [ **glTexImage2D**](glteximage2d.md)<br/>                                                                                                 |
| <span id="GL_TEXTURE_COORD_ARRAY"></span><span id="gl_texture_coord_array"></span><dl> <dt>**\_ \_ массив курд текстуры \_ GL**</dt> </dl>               | См. [ **глтекскурдпоинтер**](gltexcoordpointer.md)<br/>                                                                                       |
| <span id="GL_TEXTURE_GEN_Q"></span><span id="gl_texture_gen_q"></span><dl> <dt>**\_ \_ Общие вопросы о ТЕКСТУРе GL \_**</dt> </dl>                                 | См. [ **глтексжен**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_R"></span><span id="gl_texture_gen_r"></span><dl> <dt>**заполнение текстур главной книги \_ \_ \_**</dt> </dl>                                 | См. [ **глтексжен**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_S"></span><span id="gl_texture_gen_s"></span><dl> <dt>**\_Gen текстура GL \_ \_**</dt> </dl>                                 | См. [ **глтексжен**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_TEXTURE_GEN_T"></span><span id="gl_texture_gen_t"></span><dl> <dt>**\_Gen текстура GL \_ \_ T**</dt> </dl>                                 | См. [ **глтексжен**](gltexgen-functions.md)<br/>                                                                                               |
| <span id="GL_VERTEX_ARRAY"></span><span id="gl_vertex_array"></span><dl> <dt>**\_массив ВЕРШИН \_ GL**</dt> </dl>                                     | См. [ **глвертекспоинтер**](glvertexpointer.md)<br/>                                                                                           |



 

</dd> </dl>

## <a name="error-codes"></a>Коды ошибок

Функция [**глжетеррор**](glgeterror.md) может получить следующие коды ошибок.



| Имя                                                                                                  | Значение                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_недействительное \_ перечисление GL**</dt> </dl>      | *ограничение* не является допустимым значением.<br/>                                                                                           |
| <dl> <dt>**\_Недопустимая \_ Операция GL**</dt> </dl> | Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).<br/> |



## <a name="remarks"></a>Remarks

Функция **гллсенаблед** ВОЗВРАЩАЕТ значение GL \_ true, если *Cap* является включенной возможностью и возвращает \_ значение GL false в противном случае.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                              |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Библиотека<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**глбегин**](glbegin.md)
</dt> <dt>

[**гленабле**](glenable.md)
</dt> <dt>

[**гленд**](glend.md)
</dt> </dl>

 

 





