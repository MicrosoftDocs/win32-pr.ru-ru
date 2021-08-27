---
description: Метод Аддфаундлокатион добавляет каталог в кэш каталога.
ms.assetid: 0323c4ea-2e86-433b-87d0-34d1800a5627
title: 'Метод Имедиалокатор:: Аддфаундлокатион (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.AddFoundLocation
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ba466338e6d148e3c39a6bed4f7db413ad444ee792a4fd49b6e1499f29f0403
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051644"
---
# <a name="imedialocatoraddfoundlocation-method"></a>Метод Имедиалокатор:: Аддфаундлокатион

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`AddFoundLocation`Метод добавляет каталог в кэш каталога.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddFoundLocation(
   BSTR DirectoryName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*DirectoryName* 
</dt> <dd>

Путь к каталогу для добавления в кэш.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Указатель мультимедиа хранит кэш путей к каталогам, в которых файлы успешно найдены в прошлых поисках. После успешного нахождение файла он добавляет каталог в кэш.

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Имедиалокатор**](imedialocator.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




