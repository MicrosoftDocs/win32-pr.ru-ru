---
title: Константы D3DCOMPILE_EFFECT (D3DCompiler. h)
description: Эти константы непосредственно описывают, как компилятор компилирует файл эффектов или как среда выполнения обрабатывает файл эффектов.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986795"
---
# <a name="d3dcompile_effect-constants"></a>\_Константы эффектов D3DCOMPILE

Эти константы непосредственно описывают, как компилятор компилирует файл эффектов или как среда выполнения обрабатывает файл эффектов.

<dl> <dt>

<span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**\_ \_ Дочерний \_ эффекты D3DCOMPILE**
</dt> <dd> <dl> <dt>

(1 << 0)
</dt> <dt>



Скомпилируйте файл Effects (. FX) до дочернего эффекта. Дочерние эффекты не имеют инициализаторов для общих значений, так как эти дочерние эффекты инициализируются в главном действии (пул эффектов).

> [!Note]  
> Пулы эффектов поддерживаются эффектами 10 (FX10), но не по результатам 11 (FX11). Дополнительные сведения о различиях между пулами эффектов в Direct3D 10 и группах эффектов в Direct3D 11 см. в статье [Пулы и группы эффектов](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).

 


</dt> </dl> </dd> <dt>

<span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**\_Эффекты D3DCOMPILE \_ разрешают выполнение \_ операций с высокой скоростью \_**
</dt> <dd> <dl> <dt>

(1 << 1)
</dt> <dt>



Отключает режим производительности и позволяет применять изменяемые объекты состояния.

По умолчанию включен режим производительности. Режим производительности запрещает изменять объекты изменяемого состояния, предотвращая отображение нелитеральных выражений в определениях объектов состояния.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DCompiler. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы D3DCompiler](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

