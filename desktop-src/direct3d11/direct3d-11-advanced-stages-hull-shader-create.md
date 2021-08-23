---
title: Создание шейдера поверхности
description: В этом разделе показано, как создать шейдер поверхности.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa9fe55a11c68e4cbc247f6509c52b6bac1d01b823d48637ee51073437316f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608994"
---
# <a name="how-to-create-a-hull-shader"></a>Руководство. Создание шейдера поверхности

Шейдер поверхности — это первый из трех этапов, которые работают вместе для реализации [тесселяции](direct3d-11-advanced-stages-tessellation.md). Поверхности-шейдер выводит на этап тесселяции, а также на этап шейдера домена. В этом разделе показано, как создать шейдер поверхности.

Шейдер поверхности преобразует набор контрольных точек ввода (от шейдера вершин) в набор контрольных точек вывода. Количество входных и выходных точек может различаться в зависимости от преобразования (типичное преобразование — это преобразование «основание»).

Шейдер поверхности также выводит сведения о константе исправления, такие как факторы тесселяции, для шейдера домена и тесселяции. На этапе тесселяции с фиксированной функцией используются факторы тесселяции, а также другое состояние, объявленное в шейдере поверхности, чтобы определить, сколько нужно тесселяции.

**Создание шейдера поверхности**

1.  Создайте шейдер поверхности. См. раздел [руководство. Проектирование шейдера поверхности](direct3d-11-advanced-stages-hull-shader-design.md).
2.  Компиляция кода шейдера
3.  Создайте объект поверхности-Shader с помощью [**ID3D11Device:: креатехуллшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  Инициализируйте стадию конвейера с помощью [**ссылку ID3D11DeviceContext:: хссетшадер**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

При наличии привязки шейдера поверхности необходимо привязать шейдер домена к конвейеру. В частности, недопустимый прямой потоковая передача контрольных точек шейдера поверхности с помощью шейдера Geometry.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Общие сведения об тесселяции](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




