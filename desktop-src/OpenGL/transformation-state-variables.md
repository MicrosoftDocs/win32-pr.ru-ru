---
title: Переменные состояния преобразования
description: Переменные состояния преобразования
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Переменные состояния преобразования OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3434fe9f9aa528aa8d201b56ed363753c594690f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334275"
---
# <a name="transformation-state-variables"></a>Переменные состояния преобразования

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_ \_ Матрица моделвиев GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Описание.     | Стек матриц моделвиев             |
| Группа атрибутов: |                                    |
| Начальное значение:   | Идентификация                           |
| Команда Get:     | [**глжетфлоатв**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_матрица проекции GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Описание.     | Стек матриц проекции                                                        |
| Группа атрибутов: |                                                                                |
| Начальное значение:   | Идентификация                                                                       |
| Команда Get:     | [**глжетфлоатв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_ \_ Матрица текстур GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Описание.     | Стек матриц текстуры                                                           |
| Группа атрибутов: |                                                                                |
| Начальное значение:   | Идентификация                                                                       |
| Команда Get:     | [**глжетфлоатв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>\_окно просмотра GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Источник и экстент окна просмотра                                                       |
| Группа атрибутов: | окно просмотра                                                                         |
| Начальное значение:   |                                                                                  |
| Команда Get:     | [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_диапазон глубины \_ GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Описание.     | Диапазон глубины почти и далеко                                                       |
| Группа атрибутов: | окно просмотра                                                                       |
| Начальное значение:   | 0, 1                                                                           |
| Команда Get:     | [**глжетфлоатв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>\_ \_ глубина стека моделвиев GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Указатель стека матрицы моделвиев                                                   |
| Группа атрибутов: |                                                                                  |
| Начальное значение:   | 1                                                                                |
| Команда Get:     | [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>\_ \_ глубина стека ПРОЕЦИРОВАНия GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Указатель стека матрицы проекции                                                  |
| Группа атрибутов: |                                                                                  |
| Начальное значение:   | 1                                                                                |
| Команда Get:     | [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>\_ \_ глубина стека текстур GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Указатель стека матрицы текстуры                                                     |
| Группа атрибутов: |                                                                                  |
| Начальное значение:   | 1                                                                                |
| Команда Get:     | [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_режим матрицы GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Текущий режим матрицы                                                              |
| Группа атрибутов: | преобразование                                                                        |
| Начальное значение:   | \_МОДЕЛВИЕВ GL                                                                    |
| Команда Get:     | [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>\_нормализация GL</dt> <dd> 

|                  |                                     |
|------------------|-------------------------------------|
| Описание.     | Текущее нормальное нормализация |
| Группа атрибутов: | Преобразование или включение                    |
| Начальное значение:   | GL, \_ значение false                           |
| Команда Get:     | [**глисенаблед**](glisenabled.md)  |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>В \_ главной \_ плоскости Clip, *i*</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Описание.     | Коэффициенты для пользовательской плоскости вырезки         |
| Группа атрибутов: | преобразование                                |
| Начальное значение:   | 0, 0, 0, 0                               |
| Команда Get:     | [**глжетклипплане**](glgetclipplane.md) |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>В \_ главной \_ плоскости Clip, *i*</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Описание.     | *i* . включена плоскость обрезки пользователя |
| Группа атрибутов: | Преобразование или включение                   |
| Начальное значение:   | GL, \_ значение false                          |
| Команда Get:     | [**глисенаблед**](glisenabled.md) |



 

</dd> </dl>

 

 




