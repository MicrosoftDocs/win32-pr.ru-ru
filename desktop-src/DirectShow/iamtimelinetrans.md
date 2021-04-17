---
description: Интерфейс Иамтимелинетранс предоставляет методы для управления переходами в службах редактирования DirectShow (DES).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Интерфейс Иамтимелинетранс (Кедит. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689420"
---
# <a name="iamtimelinetrans-interface"></a>Интерфейс Иамтимелинетранс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`IAMTimelineTrans`Интерфейс предоставляет методы для управления переходами в [службах редактирования DirectShow](directshow-editing-services.md) (DES). Переход — это ход выполнения между одним видеослоем и визуализированным совмещением всех слоев видео с более низким приоритетом. Переход можно добавить к любому объекту временной шкалы, предоставляющему интерфейс [**иамтимелинетрансабле**](iamtimelinetransable.md) . Чтобы задать свойства перехода, используйте интерфейс [**ипропертисеттер**](ipropertysetter.md) .

Объект перехода DES на самом деле является оболочкой для объекта преобразования DirectX. Любой из двух входных объектов DirectX Transform можно использовать для реализации визуального влияния перехода. Корпорация Майкрософт больше не поддерживает разработку объектов преобразования DirectX сторонних производителей. Чтобы указать объект преобразования DirectX для перехода, вызовите метод [**иамтимелинеобж:: сетсубобжектгуид**](iamtimelineobj-setsubobjectguid.md) .

Чтобы создать объект перехода, вызовите [**иамтимелине:: креатимптиноде**](iamtimeline-createemptynode.md) с переходом на значение основного типа временной шкалы \_ \_ \_ . Вы можете запросить возвращенный указатель [**иамтимелинеобж**](iamtimelineobj.md) для `IAMTimelineTrans` интерфейса.

## <a name="members"></a>Элементы

Интерфейс **иамтимелинетранс** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иамтимелинетранс** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иамтимелинетранс** содержит следующие методы.



| Метод                                                  | Описание                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**жеткутпоинт**](iamtimelinetrans-getcutpoint.md)     | Извлекает вырезанную точку.<br/>                                                    |
| [**GetCutPoint2**](iamtimelinetrans-getcutpoint2.md)   | Извлекает вырезанную точку в виде значения [**рефтиме**](reftime.md) .<br/>             |
| [**жеткутсонли**](iamtimelinetrans-getcutsonly.md)     | Определяет, визуализируется ли переход как вырезание.<br/>                     |
| [**жетсвапинпутс**](iamtimelinetrans-getswapinputs.md) | Извлекает значение, указывающее, меняются ли входные данные перехода.<br/> |
| [**сеткутпоинт**](iamtimelinetrans-setcutpoint.md)     | Задает точку вырезания.<br/>                                                         |
| [**SetCutPoint2**](iamtimelinetrans-setcutpoint2.md)   | Задает точку вырезания как значение [**рефтиме**](reftime.md) .<br/>                  |
| [**сеткутсонли**](iamtimelinetrans-setcutsonly.md)     | Указывает, визуализируется ли переход как вырезание.<br/>                      |
| [**сетсвапинпутс**](iamtimelinetrans-setswapinputs.md) | Указывает, меняются ли входные данные перехода.<br/>                        |



 

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Работа с эффектами и переходами](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
