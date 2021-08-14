---
description: Можно использовать блок состояния для записи всех состояний устройства (см. раздел State Blocks Save and Restore State (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Сохранение всех состояний устройств с помощью Статеблокк (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffda5b5d637a31c774e97af85ddeca78b0995ee53c015bb2dcd245b42277a4cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520085"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a>Сохранение всех состояний устройств с помощью Статеблокк (Direct3D 9)

Можно использовать блок состояния для записи всех состояний устройства (см. раздел [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)). В состояние устройства включаются следующие элементы состояния.

-   Состояние вершины (см. раздел [Сохранение состояний вершин с помощью статеблокк (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).
-   Состояние пикселей (см. раздел [Сохранение состояния пикселей с помощью статеблокк (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).
-   Каждая текстура, назначенная для образца.
-   Каждая текстура вершин.
-   Каждая текстура карт смещения.
-   Текущая палитра текстур.
-   Для каждого потока вершин: указатель на буфер вершин, каждый аргумент из [**IDirect3DDevice9:: сетстреамсаурце**](/windows/desktop/api)и разделитель (если он есть) из [**IDirect3DDevice9:: сетстреамсаурцефрек**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).
-   Указатель на индексный буфер.
-   Окно просмотра.
-   Прямоугольник ножниц.
-   Матрицы мира, представления и проекции.
-   Преобразование текстур.
-   Обтравочные плоскости (если они есть).
-   Текущий материал.

Чтобы захватить все состояния устройств с помощью блока State, укажите D3DSBT \_ ALL при вызове [**IDirect3DDevice9:: креатестатеблокк**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Состояние блоков сохранения и восстановления](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
