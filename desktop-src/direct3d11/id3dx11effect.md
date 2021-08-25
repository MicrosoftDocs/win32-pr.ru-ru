---
title: Интерфейс ID3DX11Effect (D3dx11effect.h)
description: Интерфейс ID3DX11Effect управляет набором объектов состояния, ресурсов и шейдеров для реализации результата отрисовки.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- Интерфейс ID3DX11Effect Direct3D 11
- Интерфейс ID3DX11Effect Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4270059d02aec10905ea8aed7754bfb3a34c6897
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479150"
---
# <a name="id3dx11effect-interface"></a>Интерфейс ID3DX11Effect

Интерфейс **ID3DX11Effect** управляет набором объектов состояния, ресурсов и шейдеров для реализации результата отрисовки.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11Effect** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11Effect** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11Effect** содержит следующие методы.



| Метод                                                                     | Описание                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**клониффект**](id3dx11effect-cloneeffect.md)                           | Создает копию интерфейса Effect.<br/>                                         |
| [**жеткласслинкаже**](id3dx11effect-getclasslinkage.md)                   | Возвращает интерфейс компоновки класса.<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | Получение постоянного буфера по индексу.<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | Получение буфера констант по имени.<br/>                                                 |
| [**GetDesc**](id3dx11effect-getdesc.md)                                   | Получение описания воздействия.<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | Получите устройство, которое создало этот результат.<br/>                                        |
| [**жетграупбиндекс**](id3dx11effect-getgroupbyindex.md)                   | Возвращает группу эффектов по индексу.<br/>                                                 |
| [**жетграупбинаме**](id3dx11effect-getgroupbyname.md)                     | Возвращает группу эффектов по имени.<br/>                                                  |
| [**жеттечникуебиндекс**](id3dx11effect-gettechniquebyindex.md)           | Получение методики по индексу.<br/>                                                      |
| [**жеттечникуебинаме**](id3dx11effect-gettechniquebyname.md)             | Получите метод по имени.<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | Возвращает переменную по индексу.<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | Получить переменную по имени.<br/>                                                        |
| [**жетвариаблебисемантик**](id3dx11effect-getvariablebysemantic.md)       | Получить переменную по семантике.<br/>                                                    |
| [**Оптимизировано**](id3dx11effect-isoptimized.md)                           | Протестируйте результат, чтобы проверить, были ли метаданные отражения удалены из памяти.<br/> |
| [**IsValid**](id3dx11effect-isvalid.md)                                   | Протестируйте результат, чтобы проверить, содержит ли он допустимый синтаксис.<br/>                             |
| [**Оптимизация**](id3dx11effect-optimize.md)                                 | Сократите объем памяти, необходимый для воздействия.<br/>                          |



 

## <a name="remarks"></a>Комментарии

Результат создается путем вызова [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

Система эффектов группирует сведения, необходимые для подготовки к просмотру, в котором содержатся: объекты состояния для назначения изменений состояния в группах, ресурсы для предоставления входных данных и хранения выходных данных, а также программы, управляющие выполнением отрисовки с помощью шейдеров.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

> [!Note]
>
> При вызове [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для объекта **ID3DX11Effect** для получения интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) функция **QueryInterface** возвращает E \_ неinterface. Чтобы обойти эту ошибку, используйте следующий код:
>
> <span codelanguage=""></span>
>
> 
| | | <pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;&gt;     pIUnknown-&gt;AddRef();</code></pre> | 

>
> 
>
>  

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------|-------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |

## <a name="see-also"></a>См. также

[Effects 11, интерфейсы](d3d11-graphics-reference-effects11-interfaces.md)

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
