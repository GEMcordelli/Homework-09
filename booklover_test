import unittest
import unittest
import pandas as pd
from booklover import BookLover

class BookLoverTestSuite(unittest.TestCase):
    def test_1_add_book(self):
        test_object = BookLover("Han Solo", "hsolo@millenniumfalcon.com", "scifi")
        test_object.add_book("War of the Worlds", 4)
        self.assertTrue("War of the Worlds" in test_object.book_list['book_name'].values)
    def test2_add_book(self):
        book1 = BookLover('Bob', 'bob23@gmail.com','fantasy')
        book1.add_book('Harry Potter', 4)
        book1.add_book('Harry Potter', 4)
        self.assertEqual(book1.book_list['book_name'].value_counts().get('Harry Potter', 0), 1)
    def test_3_has_read(self):
        book1 = BookLover('Bob', 'bob23@gmail.com','fantasy')
        book1.add_book('Harry Potter', 4)
        self.assertTrue(book1.has_read('Harry Potter'))
    def test_4_has_read(self):
        book1 = BookLover('Bob', 'bob23@gmail.com','fantasy')
        book1.add_book('Lord of the Rings', 4)
        self.assertFalse(book1.has_read('Animal Farm'))
    def test_5_num_books_read(self):
        test_object = BookLover("Han Solo", "hsolo@millenniumfalcon.com", "scifi")
        test_object.add_book("War of the Worlds", 4)
        test_object.add_book('Just Mercy', 3)
        test_object.add_book('1984', 4)
        test_object.add_book('Batman', 1)
        self.assertEqual(test_object.num_books_read(), 4)
    def test_6_fav_books(self):
        book1 = BookLover('Bob', 'bob23@gmail.com','fantasy')
        book1.add_book('Dune', 4)
        book1.add_book('War of the World', 3)
        book1.add_book('1984', 4)
        book1.add_book('Batman', 1)
        fav_books = book1.fav_books()
        self.assertTrue(all(fav_books['book_rating']>3))
        
if __name__ == '__main__':
    unittest.main(argv=['first-arg-is-ignored'], verbosity = 3, exit=False)
