---
description: D3DXMATRIXA16 Structure (D3dx9math. h) — матрица 4x4, 16-байтовое с согласованием, которая содержит методы и перегрузки операторов.
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: Структура D3DXMATRIXA16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 7bb14f23d041ec2634b9710d5620382d8b93da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094212"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a>Структура D3DXMATRIXA16 (D3dx9math. h)

Матрица 4x4, 16-байтовое с согласованием, которая содержит методы и перегрузки операторов.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a>Члены

<dl> <dt>

**\_иж**
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Компонент (i, j) матрицы, где i — это номер строки, а j — номер столбца. Например, \_ 34 означает то же, что и \[ ₃ ₄ \] , компонент в третьей строке и четвертом столбце.

</dd> </dl>

## <a name="remarks"></a>Remarks

При использовании математических функций D3DX для повышения производительности процессоров Intel Pentium 4 оптимизирована сопоставленная 16-байтная матрица. Матрицы согласовываются независимо от места их создания: в стеке программы, в куче или в глобальной области. Выравнивание выполняется с помощью \_ \_ declspec (выравнивание (16)), которое работает с Visual C++ .net и Visual C++ 6,0 только при установке пакета процессора. К сожалению, нет способа обнаружить пакет процессора, поэтому выравнивание байтов по умолчанию включено только с Visual C++ .NET.

Векторы и кватернион не имеют согласованного байта в D3DX. При использовании векторов и кватернионов с математическими функциями D3DX используйте \_ declspec (выровняйте (16)) для создания векторов с согласованием байтов и кватернионов, так как они будут выполняться значительно лучше. Определение \_ declspec показано здесь.


```
#define D3DX_ALIGN16 __declspec(align(16))
```



Другие компиляторы преобразуют D3DXMATRIXA16 как D3DXMATRIX. Использование этой структуры на компиляторе, который фактически не выравнивает матрицу, может быть проблематичным, так как не будет предоставлять ошибки, не пропускаемые выравниванием. Например, если объект D3DXMATRIXA16 находится внутри структуры или класса, [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) может выполняться с плотной упаковкой (игнорируя 16-байтные границы). Это приведет к прерыванию сборки, если бы компилятору пришлось добавлять к нему выровняйте матрицу.

### <a name="d3dxmatrixa16"></a>D3DXMATRIXA16

**D3DXMATRIXA16** имеет следующие расширения C++.


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Структуры D3DX](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[**D3DXMATRIX**](d3dxmatrix.md)
</dt> </dl>

 

 
