---
title: External. showPopup, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. showPopup, метод
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- showPopup метод Windows Media Player
- showPopup метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод showPopup
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694750"
---
# <a name="externalshowpopup-method"></a>External. showPopup, метод

> [!Note]  
> В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. Использование этой функции вне контекста Интернет-магазина не поддерживается.

 

Метод **showPopup** указывает проигрывателю Windows Media отображать всплывающую веб-страницу; то есть веб-страница, которая отображается в отдельном окне.

## <a name="syntax"></a>Синтаксис


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Попупиндекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), указывающее индекс всплывающей веб-страницы.

</dd> <dt>

*Параметры* \[ окне\]
</dt> <dd>

**Строка** , добавляемая проигрывателем Windows Media в URL-адрес веб-страницы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Проигрыватель Windows Media не интерпретирует всплывающий индекс. Индексы, которые определяют всплывающие веб-страницы, создаются Интернет-магазином и имеют значение только в Интернет-магазине.

В следующих шагах показано, как проигрыватель Windows Media использует параметры метода **showPopup** для создания URL-адреса всплывающего окна.

1.  Скрипт на странице обнаружения вызывает **showPopup**, передавая целое число в *попупиндекс* и строку в *параметрах*.

2.  Проигрыватель Windows Media передает индекс в [ивмпконтентпартнер:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , чтобы получить URL-адрес отображаемой веб-страницы.

3.  Проигрыватель Windows Media добавляет *Параметры* к URL-адресу в виде строки запроса. Например, если **GetItemInfo** возвращает " https://www.Proseware.com/Pages/Popup1.htm ", а *Параметры* равны "длгкс = 800&длги = 400&приветствие = Hi", проигрыватель Windows Media создает следующий URL-адрес:

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

С помощью *параметров* можно указать размер всплывающего окна. Например, если задать для *параметров* значение "длгкс = 800&длги = 400", то всплывающее окно будет иметь размер 800 пикселей на 400 пикселей.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Внешний объект для Интернет-магазинов типа 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





