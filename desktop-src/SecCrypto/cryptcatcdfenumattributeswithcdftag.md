---
description: Перечисляет атрибуты файлов элементов в разделе Каталогфилес файла определения каталога (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: Функция Крипткаткдфенуматтрибутесвискдфтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540999"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a>Функция Крипткаткдфенуматтрибутесвискдфтаг

\[Функция **крипткаткдфенуматтрибутесвискдфтаг** доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен.\]

Функция **крипткаткдфенуматтрибутесвискдфтаг** перечисляет атрибуты файлов элементов в разделе **каталогфилес** файла определения каталога (CDF). **Крипткаткдфенуматтрибутесвискдфтаг** вызывается [макекат](makecat.md).

> [!Note]  
> Эта функция не имеет связанного файла заголовка или библиотеки импорта. Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.

 

## <a name="syntax"></a>Синтаксис


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пкдф* \[ окне\]
</dt> <dd>

Указатель на структуру [**крипткаткдф**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .

</dd> <dt>

*пвсзмембертаг* \[ окне\]
</dt> <dd>

Указатель на строку, **завершающуюся нулем,** которая определяет элемент файла каталога.

</dd> <dt>

*пмембер* \[ окне\]
</dt> <dd>

Указатель на структуру [**крипткатмембер**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) , содержащую сведения об элементе.

</dd> <dt>

*ппреваттр* \[ окне\]
</dt> <dd>

Указатель на структуру [**крипткататтрибуте**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) для атрибута элемента файла в CDF, на который указывает *пкдф*.

</dd> <dt>

*пфнпарсиррор* \[ окне\]
</dt> <dd>

Указатель на определяемую пользователем функцию для обработки ошибок синтаксического анализа файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

После успешного выполнения эта функция возвращает указатель на структуру [**крипткататтрибуте**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) . При сбое функция **крипткаткдфенуматтрибутесвискдфтаг** возвращает **пустой** указатель.

## <a name="remarks"></a>Комментарии

Обычно эта функция вызывается в цикле для перечисления всех атрибутов члена файла каталога в CDF. Перед входом в цикл задайте  для Ппреваттр **значение NULL**. Функция возвращает указатель на первый атрибут. Задайте *ппреваттр* в качестве возвращаемого значения функции для последующих итераций цикла.

## <a name="examples"></a>Примеры

В следующем примере показана правильная последовательность назначений для параметра *ппреваттр* ( `pAttr` ).


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[макекат](makecat.md)
</dt> <dt>

[**крипткататтрибуте**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[**крипткаткдф**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[**крипткатмембер**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
