---
title: Вращение Single-Finger
description: В этом разделе объясняется, как повернуть объект с помощью точки вращения.
ms.assetid: b9c19009-8ac0-4168-bf26-393280fc589f
keywords:
- Windows Сенсорный ввод, поворот
- Windows Сенсорный ввод, манипуляции
- Windows Сенсорное вращение с одним пальцем
- Windows Сенсорный ввод, поворот точки вращения
- манипуляции, вращение
- поворот, точки вращения
- вращение, одиночный палец
- жесты, вращение одним пальцем
- вращение одним пальцем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36fe7e92f6d68515e1d13b39c32ee4af5b6b03e675479242210fe302b84e6395
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110662"
---
# <a name="single-finger-rotation"></a>Вращение Single-Finger

В этом разделе объясняется, как повернуть объект с помощью точки вращения.

На следующем рисунке показан поворот с одним пальцем.

![Иллюстрация, демонстрирующая два типа поворота одного пальца: вокруг центра или вокруг края](images/sfrotation.png)

В примере а объект поворачивается вокруг центральной точки объекта с помощью жеста поворота. В примере б объект поворачивается путем перемещения одного пальца вокруг края объекта. Обработчик манипуляции включает этот поворот, используя значения «точка вращения» и «сведения о радиусе». На следующем рисунке показаны компоненты ротации с одним пальцем.

![Иллюстрация, демонстрирующая компоненты однопальцного вращения: пивотпоинткс, пивотпоинти и пивотрадиус](images/sfrotation-components.png)

После установки значений [**пивотпоинткс**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx), [**пивотпоинти**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)и [**пивотрадиус**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) в последующих сообщениях преобразования будет использоваться поворот. Чем больше значение радиуса вращения, тем больше изменений в x и y должно быть поворот объекта. В следующем коде показано, как можно задать эти значения в обработчике манипуляции.


```C++
HRESULT STDMETHODCALLTYPE CManipulationEventSink::ManipulationDelta( 
    /* [in] */ FLOAT x,
    /* [in] */ FLOAT y)
{
    m_cStartedEventCount ++;

    // Set the pivot point to the object's center and then set the radius 
    // to the distance from the center to the edge of the object.
    m_pManip->put_PivotPointX(m_objectRef->xPos);
    m_pManip->put_PivotPointY(m_objectRef->yPos);
    
    float fPivotRadius = (FLOAT)(sqrt(pow(m_dObj->get_Width()/2, 2) + pow(m_dObj->get_Height()/2, 2)))*0.4f;
    
    m_pManip->put_PivotRadius(fPivotRadius);
  

    return S_OK;
}    
     
```



В предыдущем примере расстояние до края объекта (с масштабированием до 40 процентов) используется в качестве радиуса сведения. Поскольку учитывается размер объекта, это вычисление допустимо для каждого разностного объекта. По мере масштабирования объекта радиус вращения растет. Это значение и значения Center x и y объекта передаются обработчику манипуляции для поворота объекта вокруг точки вращения.

> [!Note]  
> Значение [**пивотрадиус**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius) никогда не должно быть между 0,0 и 1,0.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Манипуляции](getting-started-with-manipulations.md)
</dt> <dt>

[**пивотрадиус**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotradius)
</dt> <dt>

[**пивотпоинткс**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx)
</dt> <dt>

[**пивотпоинти**](/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy)
</dt> </dl>

 

 




