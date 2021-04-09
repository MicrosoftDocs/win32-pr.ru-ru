---
title: Переменные состояния элемента управления буфера кадров
description: Переменные состояния элемента управления буфера кадров
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Переменные состояния элемента управления буфера кадров OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103889308"
---
# <a name="framebuffer-control-state-variables"></a>Переменные состояния элемента управления буфера кадров

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_буфер рисования \_ GL</dt> <dd> 

|                  |                                        |
|------------------|----------------------------------------|
| Описание.     | Буферы, выбранные для рисования           |
| Группа атрибутов: | цветовой буфер                           |
| Начальное значение:   |                                        |
| Команда Get:     | [**глжетинтежерв**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>\_вритемаск индекса \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Цвет — индекс вритемаск                                                            |
| Группа атрибутов: | цветовой буфер                                                                     |
| Начальное значение:   | 1                                                                              |
| Команда Get:     | [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_вритемаск цвета \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Разрешение на запись цвета; R, G, B или A                                               |
| Группа атрибутов: | цветовой буфер                                                                     |
| Начальное значение:   | значение по ГК \_                                                                         |
| Команда Get:     | [**глжетбулеанв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>\_вритемаск глубины \_ GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Буфер глубины, включенный для записи                                                 |
| Группа атрибутов: | буфер глубины                                                                     |
| Начальное значение:   | значение по ГК \_                                                                         |
| Команда Get:     | [**глжетбулеанв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_вритемаск трафарета GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Набор элементов — буфер вритемаск                                                         |
| Группа атрибутов: | набор элементов-буфер                                                                   |
| Начальное значение:   | 1                                                                              |
| Команда Get:     | [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_ \_ ясное значение цвета GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Описание.     | Очистить значение буферного цвета (режим RGBA)                                           |
| Группа атрибутов: | цветовой буфер                                                                   |
| Начальное значение:   | 0, 0, 0, 0                                                                     |
| Команда Get:     | [**глжетфлоатв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_ \_ значение очистки индекса \_ GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Описание.     | Очистить значение буфера цвета (режим индексирования цветов)                                    |
| Группа атрибутов: | цветовой буфер                                                                   |
| Начальное значение:   | 0                                                                              |
| Команда Get:     | [**глжетфлоатв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_ \_ ясное значение глубины GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Значение очистки буфера глубины                                                         |
| Группа атрибутов: | буфер глубины                                                                     |
| Начальное значение:   | 1                                                                                |
| Команда Get:     | [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_ \_ очистить значение ТРАФАРЕТа GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Описание.     | Набор элементов — очистить значение буфера                                                       |
| Группа атрибутов: | набор элементов-буфер                                                                   |
| Начальное значение:   | 0                                                                                |
| Команда Get:     | [**глжетинтежерв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>\_ \_ ясное значение НАКОПЛЕНия GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Описание.     | Накопление-значение очистки буфера                                                |
| Группа атрибутов: | накопленный буфер                                                                   |
| Начальное значение:   | 0                                                                              |
| Команда Get:     | [**глжетфлоатв**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




