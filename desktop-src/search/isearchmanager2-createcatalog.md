---
description: Создает новый пользовательский каталог в индексаторе поиска Windows и возвращает ссылку на него.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'Метод ISearchManager2:: CreateCatalog'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 009e34a2d1eb4d18df1747ba01ea39c3360ec81a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262929"
---
# <a name="isearchmanager2createcatalog-method"></a>Метод ISearchManager2:: CreateCatalog

Создает новый пользовательский каталог в индексаторе поиска Windows и возвращает ссылку на него.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*псзкаталог* \[ окне\]
</dt> <dd>

Тип: **[ **лпквстр**](../winprog/windows-data-types.md)**

Имя создаваемого каталога. Может быть любым именем, выбранным вызывающим объектом, должно содержать только стандартные алфавитно-цифровые символы и символ подчеркивания.

</dd> <dt>

*ппкаталогманажер* \[ заполняет\]
</dt> <dd>

Тип: **[ **исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***

При успешном выполнении ссылка на созданный каталог возвращается в виде указателя интерфейса [**исеарчкаталогманажер**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . Необходимо вызвать выпуск () для этого интерфейса после того, как вызывающее приложение завершит его использование.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

HRESULT, указывающий состояние операции:



| Код возврата                                                                             | Описание                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>    | Каталог ранее не существовал и был создан. Ссылка на возвращенный каталог.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | Каталог, который существовал ранее, ссылается на возвращенный каталог.<br/>                       |



 

Сбой HRESULT: не удалось создать каталог или переданы недопустимые аргументы.

## <a name="remarks"></a>Комментарии

Вызывается для создания нового каталога в индексаторе поиска Windows. После создания можно использовать методы возвращенного [**исеарчкаталог**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) Manager для добавления индексируемых расположений, отслеживания процесса индексирования и создания запросов для отправки в индексатор и получения результатов. Дополнительные сведения см. в документации по управлению индексом. https://msdn.microsoft.com/library/bb266516(VS.85).aspx

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ISearchManager2**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
