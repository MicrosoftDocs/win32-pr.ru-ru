---
description: Обсуждение мирового преобразования представляет основные понятия и предоставляет подробные сведения о настройке универсального преобразования.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Универсальное преобразование (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfbddefbaa5ad4bd41e7dafa79e086605d8f40e761cca2bd6ce9b9c0b212950a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518911"
---
# <a name="world-transform-direct3d-9"></a>Универсальное преобразование (Direct3D 9)

Обсуждение мирового преобразования представляет основные понятия и предоставляет подробные сведения о настройке универсального преобразования.

## <a name="what-is-a-world-transform"></a>Что такое универсальное преобразование?

Преобразование «мир» изменяет координаты из пространства модели, где вершины определяются по отношению к локальному источнику модели, к мировому пространству, где вершины определяются относительно источника, общего для всех объектов в сцене. По сути, мировое преобразование помещает модель в мир, — отсюда и название. На следующей схеме показана взаимосвязь между мировой системой координат и локальной системой координат модели.

![схема взаимосвязи между мировыми координатами и локальными координатами](images/worldcrd.png)

Мировое преобразование может включать любое сочетание параллельных переносов, поворотов и масштабирований.

## <a name="setting-up-a-world-matrix"></a>Установка мировой матрицы

Как и в случае с любыми другими преобразованиями, мировое преобразование создается путем с конкатенации ряда матриц в единую матрицу, которая содержит всю сумму их эффектов. В самом простом случае, когда модель находится в мировом начале координат и ее локальные координатные оси ориентированы так же, как мировое пространство, мировая матрица представляет собой единичную матрицу. Чаще, однако, мировая матрица представляет собой сочетание параллельного переноса в мировое пространство и, возможно, одного или нескольких поворотов для придания модели необходимой ориентации.

В следующем примере из вымышленного класса трехмерной модели, написанного на языке C++, используются вспомогательные функции, включенные в библиотеку служебной программы D3DX, для создания матрицы мира, которая включает три поворота для ориентации модели и перевод, чтобы переместить его относительно его положения в мировом пространстве.


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



После подготовки матрицы мира вызовите метод [**IDirect3DDevice9:: сеттрансформ**](/windows/desktop/api) , чтобы задать его, указав для первого параметра макрос [**D3DTS \_ World**](d3dts-world.md) .

> [!Note]  
> Direct3D использует установленные вами мировую матрицу и видовую матрицу для конфигурирования нескольких внутренних структур данных. Каждый раз, когда вы устанавливаете новую мировую или видовую матрицу, система пересчитывает соответствующие внутренние структуры. Частая установка этих матриц — например, несколько тысяч раз на кадр — занимает много вычислительного времени. Свести к минимуму количество необходимых вычислений можно путем конкатенации мировой и видовой матриц в мировую-видовую матрицу, задать ее в качестве мировой матрицы, а затем установить видовую матрицу в единичную. Сохраняйте кэшированные копии отдельных мировых и видовых матриц, чтобы вы могли изменять, объединять и сбрасывать мировую матрицу по необходимости. Для ясности в этой документации примеры Direct3D редко используют эту оптимизацию.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Преобразования](transforms.md)
</dt> </dl>

 

 



