---
description: DirectShow реализует IUnknown в базовом классе с именем Кункновн.
ms.assetid: 1fc74db6-c23a-464f-b9fa-b19d7e8672b7
title: Использование Кункновн
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1758065e8d618bf6ca74b37d98b0a8b5425919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663765"
---
# <a name="using-cunknown"></a>Использование Кункновн

DirectShow реализует [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) в базовом классе с именем [**кункновн**](cunknown.md). **Кункновн** можно использовать для получения других классов, переопределяя только те методы, которые изменяются между компонентами. Большинство других базовых классов в DirectShow являются производными от **кункновн**, поэтому компонент может наследовать непосредственно от **кункновн** или другого базового класса.

## <a name="inondelegatingunknown"></a>инонделегатингункновн

[**Кункновн**](cunknown.md) реализует [**инонделегатингункновн**](inondelegatingunknown.md). Он управляет внутренними счетчиками ссылок, и в большинстве случаев производный класс может наследовать два метода подсчета ссылок без изменений. Имейте в виду, что **кункновн** удаляет себя, когда счетчик ссылок становится равным нулю. С другой стороны, необходимо переопределить [**кункновн:: нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md), так как метод в базовом классе возвращает E \_ без интерфейса, если он получает идентификатор IID, отличный от \_ IUnknown. В производном классе проверьте идентификаторов IID интерфейсов, которые поддерживаются, как показано в следующем примере:


```C++
STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    if (riid == IID_ISomeInterface)
    {
        return GetInterface((ISomeInterface*)this, ppv);
    }
    // Default: Call parent class method. 
    // The CUnknown class must be in the inheritance chain.
    return CParentClass::NonDelegatingQueryInterface(riid, ppv);
}
```



Служебная функция [**IsReference**](getinterface.md) (см. Дополнительные сведения о [**вспомогательных функциях com**](com-helper-functions.md)) задает указатель, увеличивает значение счетчика ссылок потокобезопасным способом и возвращает значение S \_ ОК. В случае по умолчанию вызовите метод базового класса и возвратите результат. Если вы наследуете от другого базового класса, вызовите его метод [**нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) . Это позволяет поддерживать все интерфейсы, поддерживаемые родительским классом.

## <a name="iunknown"></a>IUnknown

Как упоминалось ранее, делегированная версия [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) одинакова для каждого компонента, так как она ничего не вызывает правильного экземпляра неделегированной версии. Для удобства файл заголовка Комбасе. h содержит макрос, [**Declare \_ IUnknown**](declare-iunknown.md), который объявляет три делегированных метода как встроенные методы. Он расширяется до следующего кода:


```C++
STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      
    return GetOwner()->QueryInterface(riid,ppv);            
};                                                          
STDMETHODIMP_(ULONG) AddRef() {                             
    return GetOwner()->AddRef();                            
};                                                          
STDMETHODIMP_(ULONG) Release() {                            
    return GetOwner()->Release();                           
};
```



Служебная функция [**кункновн::-owner**](cunknown-getowner.md) получает указатель на интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) компонента, которому принадлежит этот компонент. Для агрегированного компонента владельцем является внешний компонент. В противном случае компонент владеет самим собой. Включите макрос DECLARE \_ IUnknown в открытый раздел определения класса.

## <a name="class-constructor"></a>Конструктор класса

Конструктор класса должен вызвать метод-конструктор для родительского класса, а также все, что он делает, относящийся к вашему классу. Следующий пример является типичным методом конструктора:


```C++
CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
    : CUnknown(tszName, pUnk, phr)
{ 
    /* Other initializations */ 
};
```



Метод принимает следующие параметры, которые передаются непосредственно в метод конструктора [**кункновн**](cunknown.md) .

-   *тсзнаме* указывает имя компонента.
-   *Punk* — это указатель на агрегатный [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown).
-   *фр* — это указатель на значение HRESULT, указывающее на успешность или ошибку метода.

## <a name="summary"></a>Сводка

В следующем примере показан производный класс, который поддерживает [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) и гипотетический интерфейс с именем исомеинтерфаце:


```C++
class CMyComponent : public CUnknown, public ISomeInterface
{
public:

    DECLARE_IUNKNOWN;

    STDMETHODIMP NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if( riid == IID_ISomeInterface )
        {
            return GetInterface((ISomeInterface*)this, ppv);
        }
        return CUnknown::NonDelegatingQueryInterface(riid, ppv);
    }

    CMyComponent(TCHAR *tszName, LPUNKNOWN pUnk, HRESULT *phr) 
        : CUnknown(tszName, pUnk, phr)
    { 
        /* Other initializations */ 
    };

    // More declarations will be added later.
};
```



В этом примере показаны следующие моменты.

-   Класс [**кункновн**](cunknown.md) реализует интерфейс [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Новый компонент наследует от **кункновн** и от всех интерфейсов, поддерживаемых компонентом. Компонент может быть производным от другого базового класса, наследующего от **кункновн**.
-   Макрос [**Declare \_ IUnknown**](declare-iunknown.md) объявляет делегированные методы [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) как встроенные методы.
-   Класс [**кункновн**](cunknown.md) предоставляет реализацию для [**инонделегатингункновн**](inondelegatingunknown.md).
-   Для поддержки интерфейса, отличного от [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), производный класс должен переопределить метод [**нонделегатингкуеринтерфаце**](cunknown-nondelegatingqueryinterface.md) и проверить идентификатор IID нового интерфейса.
-   Конструктор класса вызывает метод конструктора для [**кункновн**](cunknown.md).

Следующим шагом при написании фильтра является предоставление приложению возможности создавать новые экземпляры компонента. Это требует понимания библиотек DLL и их связи с фабриками классов и методами конструктора классов. Дополнительные сведения см. [в разделе Создание библиотеки DLL фильтра DirectShow](how-to-create-a-dll.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Реализация IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 
