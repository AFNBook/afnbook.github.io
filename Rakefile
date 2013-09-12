require './Rakefile-octopress'

ENV['book_source'] = File.join(File.expand_path(File.dirname(__FILE__)), '/source/_book')
ENV['book_path'] = File.join(File.expand_path(File.dirname(__FILE__)), '/source/book')

namespace :book do
	desc "Generar libro"
	task :generate do
		FileUtils.mkpath ENV['book_path']

		#recorro todos los directorios de dentro del book_path
		chapters_path = File.join(ENV['book_source'], 'chapters/*')

		Dir[chapters_path].each do |chapter_folder|
			puts chapter_folder
		end
	end

	desc "Delete generated book"
	task :clean do
		FileUtils.remove_dir ENV['book_path']
		puts "Removing output #{ENV['book_path']}"
	end
end